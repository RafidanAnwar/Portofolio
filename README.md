# Portofolio Ummu Radiah

Proyek ini adalah halaman portofolio pribadi statis milik Ummu Radiah, S.Kom, yang menampilkan profil, proyek-proyek, dan sertifikat. Halaman ini dibangun menggunakan HTML murni dan CSS.

## 🚀 Status Deployment (Vercel)
✅ **Live & Deployed Successfully**

### 🐛 Log Perbaikan Bug Deployment
Sempat terjadi dua kendala pada saat pertama kali proyek ini di-deploy ke Vercel:

1. **Error 404 NOT_FOUND pada Halaman Utama (Root)**
   * **Penyebab:** Sistem Vercel berjalan pada lingkungan Linux yang bersifat *case-sensitive* (membedakan huruf besar dan kecil). File HTML utama pada proyek ini sebelumnya bernama `Index.html` (dengan huruf 'I' besar), sedangkan Vercel mencari file bernama `index.html`.
   * **Solusi:** Mengubah nama file dari `Index.html` menjadi `index.html` dan melakukan *push* ulang ke repositori GitHub.

2. **Error 404 pada `/favicon.ico`**
   * **Penyebab:** Browser secara otomatis mencari file `favicon.ico` untuk dijadikan ikon tab. Karena belum ada file ikon yang disediakan dalam proyek, browser memunculkan error 404 di Console.
   * **Solusi:** Menambahkan kode `<link rel="icon" href="data:,">` pada bagian `<head>` di file `index.html`. Ini menginstruksikan browser untuk menggunakan data URI kosong dan tidak melakukan request file ke server.

Semua masalah di atas kini telah teratasi sepenuhnya, dan website berjalan dengan sempurna di Vercel.

---
*Dokumen ini dibuat otomatis untuk mendokumentasikan log perbaikan deployment Vercel.*
