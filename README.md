

# Efisiensi Anggaran Menggunakan Monte Carlo Simulation
Repository ini berisi analisis **efisiensi anggaran belanja kegiatan** menggunakan pendekatan **Monte Carlo Simulation**. Project ini bertujuan untuk mengukur potensi penghematan anggaran secara realistis dengan mempertimbangkan batasan kebijakan, kategori belanja, serta pagu minimum dan maksimum anggaran.
## Tujuan Analisis
1. Mengestimasi potensi **penghematan anggaran** secara probabilistik.
2. Menentukan **rentang efisiensi yang wajar** berdasarkan kategori belanja.
3. Menilai apakah target efisiensi dapat dicapai tanpa melanggar **pagu minimum anggaran**.
4. Memberikan **rekomendasi efisiensi berbasis data** pada setiap item belanja.



## Metodologi
Analisis dilakukan dengan:
* Mengelompokkan item belanja ke dalam kategori:
  * **TIDAK BOLEH DIPOTONG**
  * **TERBATAS**
  * **PRIORITAS**
* Menentukan rentang persentase efisiensi untuk setiap kategori.
* Menjalankan **Monte Carlo Simulation (100.000 iterasi)** untuk:
  * Simulasi total penghematan
  * Simulasi total anggaran setelah efisiensi
* Memvalidasi hasil terhadap **pagu minimum anggaran**



## Visualisasi Hasil
### 1. Distribusi Penghematan Anggaran (Monte Carlo)
<img width="859" height="547" alt="image" src="https://github.com/user-attachments/assets/4b80cd6f-e569-4a0f-82f7-5267e81d64d8" />

Grafik ini menunjukkan sebaran nilai penghematan anggaran dari seluruh simulasi.
Garis vertikal putus-putus menandai target efisiensi.
Interpretasi:
* Distribusi relatif simetris dan stabil
* Mayoritas simulasi menghasilkan penghematan **di atas target**
* Menunjukkan konsistensi kebijakan efisiensi



### 2. Distribusi Total Anggaran Setelah Efisiensi
<img width="1014" height="547" alt="image" src="https://github.com/user-attachments/assets/4dbe4a7e-b718-4fff-89ce-8986fe6f6d9f" />

Grafik ini memperlihatkan total anggaran akhir setelah efisiensi.
Interpretasi:
* Seluruh hasil simulasi berada di antara **pagu minimum dan maksimum**
* Tidak ada pelanggaran batas anggaran
* Efisiensi tetap menjaga keberlangsungan operasional



##  Tabel Ringkasan Hasil Monte Carlo

| Metric                        | Nilai (Rp)  |
| ----------------------------- | ----------- |
| Total Anggaran Dianalisis     | 164,744,922 |
| Rata-rata Penghematan         | 25,160,771  |
| Persentil 95%                 | 29,832,949  |
| Best Case                     | 33,140,905  |
| Worst Case                    | 17,254,694  |
| Probabilitas Capai Target (%) | **97%**     |

**Interpretasi:**
* Rata-rata efisiensi mencapai ± **15% dari total anggaran**
* Probabilitas mencapai target efisiensi sangat tinggi (**97%**)
* Risiko gagal mencapai target relatif rendah



## Seluruh Rekomendasi Efisiensi Anggaran
| Kode | Uraian                                    | Koefisien | Satuan | Harga (Rp) | Total (Rp) | Kategori             | Persen Efisiensi | Estimasi Hemat (Rp) |
| ---- | ----------------------------------------- | --------- | ------ | ---------- | ---------- | -------------------- | ---------------- | ------------------- |
| 23   | Belanja Jasa Pelayanan Kesehatan Bagi ASN | 1         | Tahun  | 96,782,400 | 96,782,400 | TERBATAS             | Variabel         | 11,923,533          |
| 31   | Jasa Pengelola BMD Pembantu               | 12        | Bulan  | 600,000    | 7,200,000  | PRIORITAS            | Variabel         | 2,157,585           |
| 97   | Foto Copy F4 70 gr                        | 6,630     | Lembar | 700        | 4,641,000  | PRIORITAS            | Variabel         | 1,607,150           |
| 63   | Kertas HVS F4                             | 25        | Rim    | 131,900    | 3,297,500  | PRIORITAS            | Variabel         | 1,180,870           |
| …    | …                                         | …         | …      | …          | …          | …                    | …                | …                   |
| 16   | Belanja Iuran Jaminan Kesehatan PPPK      | 1         | Tahun  | 1,869,669  | 1,869,669  | TIDAK BOLEH DIPOTONG | 0                | 0                   |
| 11   | Belanja Iuran Jaminan Kesehatan PNS       | 1         | Tahun  | 3,253,753  | 3,253,753  | TIDAK BOLEH DIPOTONG | 0                | 0                   |

 **Catatan:**
Item dengan kategori **TIDAK BOLEH DIPOTONG** tidak dikenakan efisiensi sesuai kebijakan.



## Tabel Pagu & Hasil Efisiensi
| Keterangan                  | Nilai (Rp)  |
| --------------------------- | ----------- |
| Total Anggaran Awal         | 164,744,922 |
| Pagu Maksimum               | 164,744,922 |
| Pagu Minimum                | 131,795,938 |
| Rata-rata Setelah Efisiensi | 139,591,155 |
| Efisiensi Rata-rata         | 25,153,767  |
**Interpretasi:**
* Anggaran akhir **tetap di atas pagu minimum**
* Efisiensi tidak mengganggu kelangsungan program
* Memberikan ruang fiskal yang sehat



## Kesimpulan
1. Monte Carlo Simulation efektif untuk memodelkan efisiensi anggaran berbasis risiko.
2. Target efisiensi sangat **realistis dan aman secara kebijakan**.
3. Efisiensi terbesar berasal dari belanja kategori **PRIORITAS** dan **TERBATAS**.
4. Pendekatan ini dapat digunakan sebagai **alat bantu pengambilan keputusan anggaran**.





