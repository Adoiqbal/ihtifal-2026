# Ihtifal 2026: Buku Program Digital

Buku program digital beranimasi untuk **Majlis Anugerah Kecemerlangan dan Graduasi SMIIPSU | EHSAN 2026**
(4 Disember 2026, Dewan Kuliah 500, UiTM Puncak Alam).

## Kandungan laman
- Kulit dengan tirai batik dan kiraan detik ke majlis
- Sekapur Sirih, Atur Cara, Objektif, Senarai Jawatankuasa
- Penerima Anugerah EHSAN mengikut tahap (Prasekolah, Tahun 1 hingga 6)
- Semak Nama Anak dan Kad Anugerah (1080×1350) untuk media sosial
- Anugerah Khas dirahsiakan sehingga hari majlis (nama penerima tidak disimpan dalam kod)

## Struktur
```
index.html   laman (HTML, CSS dan JS dalam satu fail)
img/         aset batik, logo dan gambar murid
js/          GSAP 3.12.5 + ScrollTrigger (disimpan setempat, tiada CDN)
```

## Kemas kini data
Semua data penerima ada dalam `index.html`, di bahagian `/* ================= DATA ================= */`
(`KEDUDUKAN`, `SUBJEK`, `GRADUASI`, `TERBAIK_PRA`, `SAHSIAH`).

## Hosting
Laman statik. Aktifkan GitHub Pages: Settings → Pages → Deploy from branch → `main` / root.
