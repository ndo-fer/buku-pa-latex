# Cara menerapkan patch BAB 4

Patch ini mengganti `chapters/bab4.tex` dengan versi revisi penuh.

Jalankan dari root repo `buku-pa-latex`:

```bash
rm chapters/bab4.tex
git apply /path/to/bab4_replace.patch
git add chapters/bab4.tex
git commit -m "Revisi BAB 4 eksperimen dan analisis pseudo-label"
git push origin main
```

Alternatif tanpa `git apply`:

```bash
cp chapters/bab4.tex /path/to/buku-pa-latex/chapters/bab4.tex
cd /path/to/buku-pa-latex
git add chapters/bab4.tex
git commit -m "Revisi BAB 4 eksperimen dan analisis pseudo-label"
git push origin main
```

Catatan:
- Patch ini memakai gambar yang sudah ada di folder `media/media/` dari repo.
- BAB 4 direvisi agar metrik dievaluasi terhadap pseudo-label, bukan fraud ground truth.
- Narasi leakage/performance inflation sudah ditambahkan pada bagian benchmarking dan final evaluation.
