# Moora App

Moora App adalah aplikasi web yang menggunakan metode MOORA (Multi-Objective Optimization on the basis of Ratio Analysis) untuk melakukan perankingan alternatif berdasarkan bobot kriteria dan nilai alternatif. Aplikasi ini dibangun menggunakan React/18.2.0, React-DOM/18.2.0, Babel Standalone/7.21.1, Bootstrap/5.3.0, dan Visual Studio Code.

## Demo

Aplikasi ini dapat diakses melalui tautan berikut: [Moora App](https://amber-zandra-48.tiiny.site/)

![image](https://github.com/fantasiavsr/mooraapp/assets/86558365/0e76314f-239f-472a-a603-11a601da871d)

## Fitur

- [Rumus Moora]
- [Cara Penggunaan]
- [Data Alternatif]
- [Bobot Kriteria]
- [Normalisasi]
- [Optimasi]
- [Hasil Ranking]

## Rumus Moora

Rumus Moora digunakan untuk menghitung perankingan alternatif berdasarkan bobot kriteria dan nilai alternatif. Berikut adalah langkah-langkah dalam perhitungan Moora:

### Normalisasi Matriks

Untuk setiap kriteria, hitung nilai normalisasi alternatif dengan menggunakan rumus berikut:
```shell
normalizedValue = value / sqrt(sum of squares)
```
### Perhitungan Nilai Optimasi

Jika kriteria berupa benefit, gunakan rumus berikut:
```shell
optimizationValue = (weight * (alternative[criterion.name] - minValue)) / (maxValue - minValue)
```
Jika kriteria berupa cost seperti "jarakRumah", "pajakPpn", atau "hargaParkir", gunakan rumus berikut:
```shell
optimizationValue = (weight * (maxValue - alternative[criterion.name])) / (maxValue - minValue)
```

### Perankingan Alternatif

Jumlahkan nilai optimasi untuk setiap alternatif dan urutkan alternatif berdasarkan skor tertinggi.

Sumber: [Multi-Objective Optimization on the basis of Ratio Analysis](https://example.com)

## Cara Penggunaan

1. Generate data alternatif terlebih dahulu dengan mengklik tombol "Generate Alternatif".
2. Isi bobot kriteria dengan nilai antara 0 dan 1. Setidaknya satu bobot harus diisi dan tidak boleh 0.
3. Setelah mengisi bobot kriteria, klik tombol "Hitung" untuk menghitung perankingan alternatif.
4. Hasil perankingan alternatif akan ditampilkan dalam tabel dengan alternatif yang memiliki skor tertinggi berada di posisi atas.

Catatan: Pastikan untuk mengisi semua kriteria dengan benar dan mempertimbangkan kebutuhan dan preferensi Anda saat memberikan bobot.

