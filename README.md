<div align="center">

# BiWeather

**Front-end aplikasi prediksi cuaca untuk tugas mata kuliah AI.**

![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-3-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)

</div>

## Tentang

BiWeather menampilkan prakiraan cuaca untuk lokasi yang dicari: kondisi saat ini, prakiraan per jam, prakiraan harian, analisis risiko, rekomendasi aktivitas, dan ringkasan dampak ekonomi.

> Proyek ini murni front-end. Data cuaca dihasilkan oleh `src/data/mockWeatherData.ts`, belum terhubung ke API cuaca sungguhan.

## Fitur

- Pencarian lokasi dan pemilihan sumber data `API` / `Sensor` (keduanya masih simulasi).
- Ringkasan kondisi saat ini: suhu, kelembapan, angin, dan status cuaca.
- Prakiraan per jam dan prakiraan beberapa hari ke depan.
- Analisis risiko cuaca dan rekomendasi aktivitas.
- Ringkasan dampak ekonomi dari kondisi cuaca.
- Loading state, toast notifikasi, dan tombol refresh manual.

## Menjalankan

```bash
npm install
npm run dev      # http://localhost:5173
npm run build
npm run lint
```

## Struktur

```
src/
├── pages/Index.tsx              # halaman utama, pengatur state dan data
├── components/weather/          # widget cuaca (current, hourly, daily, risk, dll.)
├── data/mockWeatherData.ts      # generator data cuaca simulasi
├── types/weather.ts             # tipe WeatherData
└── components/ui/               # komponen shadcn/ui
```

## Menghubungkan Data Nyata

Semua data masuk lewat `fetchWeatherData` di `src/pages/Index.tsx`. Ganti pemanggilan `generateMockWeatherData(loc)` dengan request ke API pilihanmu (misalnya OpenWeatherMap), lalu petakan responsnya ke tipe `WeatherData`. Komponen tidak perlu diubah.

---

Dibuat oleh [Rizky Putra Ichfiandra](https://github.com/RizkyPutraIchfiandra).
