# Tugas 05 – Transfer Learning untuk Klasifikasi Citra dengan Data Terbatas

**Nama:** Jos Hwen Sim
**NIM:** 280-245-1655

## Deskripsi
Perbandingan ResNet-18 pada subset 10 kelas Oxford-IIIT Pet dengan tiga
paradigma: training from scratch (B1), feature extraction (B2), dan
progressive fine-tuning (B3). Dilengkapi uji kontrol data augmentation (B4)
dan visualisasi Grad-CAM pada layer4.

## Cara Menjalankan
1. Buka `Code.ipynb` di Google Colab (runtime GPU T4).
2. Install dependensi: `pip install -r requirements.txt`
3. Jalankan Runtime → Run all.

Dataset terunduh otomatis lewat `torchvision.datasets.OxfordIIITPet`
(tidak disertakan di repo).

## Konfigurasi Eksperimen
- Seed: 42
- Batch size: 32, optimizer AdamW, loss CrossEntropyLoss
- Split: 70/15/15 stratified, 10 kelas
- Early stopping: patience <3–5> pada validation loss

## Struktur Berkas
| File | Keterangan |
|---|---|
| `Code.ipynb` | Notebook eksperimen |
| `requirements.txt` | Daftar dependensi |
| `LaporanHasilEksperimen.pdf` | Laporan hasil eksperimen |
| `Jawaban Bagian A.pdf` | Jawaban analisis konseptual (Bagian A) |
| `results_summary.csv` / `.json` | Ringkasan metrik tiap eksperimen |
| `history_per_epoch.csv` | Log loss & akurasi per epoch |
| `b4_augmentation_comparison.csv` | Hasil uji augmentasi |
| `per_class_report_best_model.csv` | Laporan per kelas model terbaik |
| `failure_samples.csv` | Daftar sampel misklasifikasi |
| `learning_curves.png` | Kurva training vs validation loss |
| `failure_analysis.png` | Visualisasi failure analysis |
| `gradcam_layer4.png` | Visualisasi Grad-CAM layer4 |

## Referensi & Pernyataan AI
Lihat bagian akhir laporan.
