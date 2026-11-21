# muhemed crackme — Static Password Reconstruction

| Field | Value |
|---|---|
| Source | [Crackmes.one](https://crackmes.one/crackme/6a7b401905a9e80a90724367) |
| Activity | Latihan reverse engineering mandiri; bukan kompetisi CTF |
| Format | Linux ELF (as recorded in the lab notes) |
| Difficulty | 1.0 / 6.0 (as listed in the original note; may change on the source platform) |
| Primary tool | `file`, `rabin2`, `radare2` |

## Goal

Determine how the program validates its password without assuming that a printable password string must be present in the ELF string table.

## Initial inspection

```bash
file crackme
rabin2 -z crackme
r2 -q -e scr.color=0 crackme
```

In the recorded run, `rabin2 -z` did not reveal the password as a normal string. That is a useful negative observation, not proof that the value is encrypted.

## Static-analysis path

```text
aaa
afl
pdf @ dbg.main
```

The existing analysis notes report that the program constructs the candidate password from three 64-bit values written on the stack and compares the result with the user input through `strcmp`. The recorded candidate is:

```text
wvohXN8X7C14jrq1F*!j
```

This points to data hiding / constant reconstruction rather than evidence of cryptographic encryption. The password is shown here because it is part of the author's learning note; follow Crackmes.one rules before publishing solutions to any other challenge.

## Verification status and limitations

The notes inherited into this pack do not include a full instruction-by-instruction transcript or a current binary hash. Before describing this analysis as fully reproducible, rerun the source binary, record its SHA-256, preserve the exact relevant disassembly (without unrelated output), and verify the input/output in a disposable VM. Do not infer a new vulnerability or general weakness from this crackme alone.

## Lessons

- Use `file` and section/string inspection to build initial hypotheses, not conclusions.
- Follow data flow from input to comparison in the disassembly.
- Stack constants can encode human-readable strings due to byte order; reconstruct bytes carefully.
- Record tool versions, offsets, and verification output so another person can repeat the result.

## Related repository structure

This is the single canonical write-up for this challenge. `reverse-engineering-lab` contains a short pointer to this file rather than a second full copy.
