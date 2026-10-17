# Buku Saku Kredit Perbankan

Website satu halaman tentang perbankan, khususnya kredit/pinjaman. Tampilannya tenang (terinspirasi pipdot.app), dengan sidebar menu (laci di HP), mode terang/gelap, dan sistem tag lintas halaman. Lima menu utama:

## 1. Glosarium (350+ istilah)
- Pencarian langsung di nama istilah, singkatan, dan isi definisi
- Filter 11 kategori: produk kredit, analisis & proses, agunan & hukum, bunga & biaya,
  kualitas & kredit bermasalah, prudensial OJK, moneter/makroprudensial/sistem pembayaran BI,
  lembaga, syariah, konsumen & fintech, akuntansi & rasio
- Navigasi A–Z
- Tiap istilah menautkan aturan yang menjadi dasarnya

## 2. Regulasi OJK & BI (50+ aturan)
- Undang-undang & pemerintah: UU Perbankan, UU P2SK, UU BI, UU OJK, UU LPS, UU Hak Tanggungan,
  UU Fidusia, UU Kepailitan, UU PDP, PP 47/2024, Permenko KUR 2026, dll.
- OJK: POJK kualitas aset, BMPK, KPB, manajemen risiko, tingkat kesehatan, KPMM, SLIK,
  pelindungan konsumen & etika penagihan, pinjaman daring, restrukturisasi bencana, UMKM, dll.
- Bank Indonesia: BI-Rate, LTV/FTV (PADG 30/2025), GWM, RIM/PLM, RPIM, KLM, CCyB,
  sistem pembayaran, kartu kredit
- LPS: penjaminan simpanan & tingkat bunga penjaminan
- Filter per penerbit, pencarian nomor/topik, dan tautan ke istilah terkait di glosarium

## 3. Materi
11 bab rangkuman materi kredit dengan definisi, tabel, rumus, dan contoh soal.

## 4. Simulasi (lembar kerja)
Format Diketahui / Ditanya / Jawab dengan langkah perhitungan:
1. Angsuran kredit flat, efektif, anuitas + jadwal angsuran
2. Konversi bunga flat ke bunga efektif
3. Kemampuan bayar dan plafon KPR maksimum (DSR, LTV)
4. Kolektibilitas dan PPKA (POJK 40/2019)
5. Cek biaya pinjaman daring terhadap batas OJK 2026

## 5. Latihan soal
12 soal pilihan ganda dengan pembahasan.

## Tag
Tag (mis. `#kpr`, `#agunan`, `#pinjol`) menghubungkan istilah, peraturan, bab materi, dan lembar kerja.
Klik tag untuk melihat semua item terkait. Menambah tag cukup lewat daftar `TAGS` di `public/index.html`
(aturan otomatis untuk istilah), `REG_TAGS` untuk peraturan, dan atribut `data-tags` untuk bab/lembar kerja.

## Cara membuka
Tidak perlu build. Seluruh situs ada di satu file, `public/index.html`; buka langsung di browser.

## Deploy ke Cloudflare (gratis)
Repo ini sudah berisi `wrangler.jsonc` yang mengunggah folder `public/` sebagai static assets
di Cloudflare Workers. Permintaan ke static assets gratis, juga di paket Free.

Di dashboard Cloudflare (Workers & Pages → Create → Import a repository):
- Project name: `super-duper-happiness` (harus sama dengan `name` di `wrangler.jsonc`)
- Build command: kosongkan
- Deploy command: `npx wrangler deploy`

Situs akan tersedia di `super-duper-happiness.<subdomain-akun>.workers.dev`, dan setiap push
ke branch production otomatis di-deploy ulang.

Isi regulasi dicek per Oktober 2026. Aturan dapat berubah; untuk keperluan resmi
selalu rujuk teks lengkap di ojk.go.id, bi.go.id, lps.go.id, atau JDIH.
