# CTF Write-ups & Challenge Research Notes

Repository ini menyimpan **write-up teknis orisinal** untuk dua jenis aktivitas:

1. **Independent practice** — challenge mandiri, crackme, wargame, dan authorized training lab.
2. **Official competitions** — write-up challenge kompetisi yang hanya dipublikasikan setelah event dan hanya jika aturan resmi mengizinkannya.

Repository ini adalah satu-satunya tempat untuk **full challenge write-up**. Jangan menggandakan full solusi ke `ctf-track-record` atau `reverse-engineering-lab`.

## Repository map

| Path | Fungsi |
|---|---|
| [`practice/`](practice/README.md) | Write-up latihan mandiri dan training lab. |
| [`competitions/`](competitions/README.md) | Write-up challenge kompetisi pasca-event yang publikasinya diizinkan. |
| [`templates/`](templates/) | Template write-up dan pemeriksaan publikasi. |

## Current write-ups

- [XorGate Crackme](practice/Crackmes.one/XorGate.md) — username-dependent password derivation using an XOR/hex transformation.
- [muhemed crackme](practice/Crackmes.one/muhemed-crackme.md) — reconstruction of a static password from stack constants.

Keduanya merupakan latihan mandiri dari Crackmes.one, bukan klaim hasil kompetisi resmi atau penemuan kerentanan dunia nyata.

## Rules before publishing

- Periksa aturan platform atau event yang berlaku untuk challenge tersebut.
- Untuk kompetisi, tunggu event berakhir dan pastikan embargo/publication window sudah lewat.
- Pastikan aturan mengizinkan publikasi **solusi lengkap**, bukan hanya pembahasan umum.
- Sensor atau menghapus flag tidak otomatis membuat full solusi boleh dipublikasikan.
- Jika status izin tidak jelas atau publikasi dilarang, simpan catatan secara privat/lokal dan jangan masukkan ke repository publik.
- Jangan unggah credentials, data pribadi, secrets, source/binary challenge, screenshot, atau aset pihak ketiga tanpa hak/izin redistribusi.
- Catat sumber, tanggal pemeriksaan aturan, status publikasi, dan batasan reproduksi.

Gunakan [`templates/TEMPLATE-WRITEUP.md`](templates/TEMPLATE-WRITEUP.md) untuk write-up dan [`templates/TEMPLATE-PUBLICATION-CHECK.md`](templates/TEMPLATE-PUBLICATION-CHECK.md) untuk event yang memerlukan pemeriksaan izin publikasi tersendiri.

## Relationship to other repositories

- [`ctf-track-record`](https://github.com/madanisora/ctf-track-record) menyimpan **rekam keikutsertaan kompetisi resmi**: event, tanggal, format individu/tim, scoreboard, dan hasil yang terverifikasi. Tidak menyimpan full solusi.
- [`reverse-engineering-lab`](https://github.com/madanisora/reverse-engineering-lab) menyimpan **artefak teknis yang berdiri sendiri**: tools, script reusable, harness, eksperimen fuzzing, crash reproducer, log terpilih, regression test, dan laporan root-cause. Repository itu boleh menautkan write-up kanonis, tetapi tidak menyalin full write-up.

## License

Original written write-ups, explanations, and documentation authored by MadaniSora in this repository are licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/), as stated in the root `LICENSE` file.

The CC BY 4.0 license applies only to material that MadaniSora owns and is authorized to license. It does not apply to third-party challenge binaries, challenge source files, platform content, flags, screenshots, logos, images, datasets, or other externally owned material.

Original short code excerpts embedded in a write-up are presented as explanatory parts of that document. This repository is not the distribution home for standalone reusable software. A reusable program, tool, or script should be maintained in `reverse-engineering-lab` and have an explicit software license there. Creative Commons recommends using a software-specific license rather than a CC license for software itself; see the [Creative Commons FAQ](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software).

Third-party material remains subject to its own license, permission, copyright, and platform publication rules. A link to a challenge is preferred to redistributing its files when permission is not explicit.
