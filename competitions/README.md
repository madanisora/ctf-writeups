# Post-event competition write-ups

Folder ini khusus untuk **full challenge write-ups dari kompetisi resmi** yang boleh dipublikasikan setelah event.

## Publication gate

Sebelum membuat file publik:

1. Event sudah resmi berakhir.
2. Embargo atau publication window sudah berakhir.
3. Aturan resmi mengizinkan publikasi solusi lengkap (bukan hanya flag disensor).
4. Aturan flag, source code, binary, screenshot, dan materi penyelenggara sudah diperiksa.
5. Jika perlu review/approval penyelenggara, approval sudah diterima.

Simpan pemeriksaan tersebut di `PUBLICATION-CHECK.md` dalam folder event. Gunakan [`templates/TEMPLATE-PUBLICATION-CHECK.md`](../templates/TEMPLATE-PUBLICATION-CHECK.md).

## Folder convention

```text
competitions/
├── README.md
└── YYYY/
    └── <event-slug>/
        ├── PUBLICATION-CHECK.md
        └── <category>/
            ├── <challenge-one>.md
            └── <challenge-two>.md
```

Buat folder event hanya setelah izin publikasi dinyatakan jelas. Jangan masukkan solusi saat event berlangsung, solusi yang dilarang, atau materi pihak ketiga yang tidak boleh didistribusikan. Redaksi flag tidak otomatis mengizinkan publikasi full solution.

`ctf-track-record` menyimpan catatan bahwa event benar-benar diikuti dan hasil terverifikasi. Repository ini menyimpan pembahasan challenge yang publikasinya diizinkan. Jangan menyalin scoreboard, sertifikat, atau full event record ke setiap write-up.
