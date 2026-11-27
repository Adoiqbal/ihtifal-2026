# Ihtifal 2026: Buku Program Digital

Buku program digital beranimasi untuk **Majlis Anugerah Kecemerlangan dan Graduasi SMIIPSU | EHSAN 2026**
(4 Disember 2026, Dewan Kuliah 500, UiTM Puncak Alam).

## Kandungan laman
- Kulit dengan tirai batik dan kiraan detik ke majlis
- Sekapur Sirih, Atur Cara, Objektif, Senarai Jawatankuasa
- Penerima Anugerah EHSAN mengikut tahap (Prasekolah, Tahun 1 hingga 6)
- Semak Nama Anak dan Kad Anugerah (1080×1350) untuk media sosial
- Anugerah Khas dirahsiakan sehingga hari majlis (nama penerima tidak disimpan dalam kod)

## Tema rasmi
“Menyemai Akhlak, Menjulang Ilmu, Menabur Bakti”

## Struktur
```
index.html   laman (HTML, CSS dan JS dalam satu fail)
img/         aset batik, logo dan gambar murid
js/          GSAP 3.12.5 + ScrollTrigger (disimpan setempat, tiada CDN)
audio/       (pilihan) fail muzik latar dan bunyi anugerah — lihat bahagian Audio
```

## Kemas kini data
Semua data penerima ada dalam `index.html`, di bahagian `/* ================= DATA ================= */`
(`KEDUDUKAN`, `SUBJEK`, `GRADUASI`, `TERBAIK_PRA`, `SAHSIAH`).

## Hosting
Laman statik di GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).
Domain: **https://ihtifal.ehsanschool.edu.my** (fail `CNAME`). DNS diurus di Cloudflare:
rekod `CNAME ihtifal → adoiqbal.github.io`, status *DNS only*. Jika nameserver domain ditukar
kemudian, rekod ini mesti ditambah semula di penyedia DNS baharu.

## Gambar penerima
Gambar dipaparkan dalam nisbah 4:5 (bahu ke atas). Kedudukan crop setiap gambar ditetapkan dalam
`PHOTO_FOCUS` dalam `index.html` (pecahan `x`, `y`, `w`, `h` bagi fail asal). Laraskan nilai di situ
jika crop perlu dibetulkan; fail gambar asal tidak diubah. Gambar tanpa konfigurasi guna
`object-fit: cover` sebagai asas.

## Audio
Audio hanya untuk pengalaman pengunjung laman (bukan untuk dewan). Tiada bunyi dimainkan secara
automatik; muzik latar bermula hanya selepas pengunjung menekan butang audio.

Secara lalai, muzik latar dan fanfare anugerah dijana secara digital dalam pelayar (Web Audio API),
jadi tiada fail dan tiada isu hak cipta. Untuk guna fail sendiri:

1. Letakkan fail dalam folder `audio/` (MP3 disokong semua pelayar utama).
2. Kemas kini `AUDIO_SRC` dalam `index.html`, contohnya `{music:'audio/<fail-muzik>.mp3', award:'audio/<fail-fanfare>.mp3'}`.
3. Jika fail gagal dimuat, laman kembali kepada bunyi digital secara automatik.

Fail yang diperlukan (jika mahu ganti bunyi digital):
- Muzik latar instrumental, 1–3 minit, boleh diulang (loop) dengan lancar, ±128 kbps, kurang 3 MB.
- Fanfare anugerah, 1–2 saat, kurang 100 KB.
Pastikan fail mempunyai lesen yang membenarkan penggunaan (contohnya ciptaan sendiri atau lesen bebas royalti).

## Buku program (PDF)
Letakkan fail PDF di `pdf/buku-program-ihtifal-2026.pdf` (nama mesti tepat). Butang "Muat Turun PDF"
dan "Buka" dalam seksyen Buku Program Digital aktif secara automatik bila fail wujud; jika tiada,
laman memaparkan "akan dimuat naik tidak lama lagi". Saiz disyorkan bawah 20 MB.

## Tirai pembuka
Tirai batik di kulit tertutup semasa laman dibuka dan terbuka pada interaksi pertama (sentuh, klik,
tatal atau kekunci). Pautan terus ke bahagian lain (contohnya `#penerima`) melangkau tirai.
