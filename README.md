🎬 VelyStream

«Modern Anime Streaming App for Android
Watch your favorite anime with a clean, fast, and cinematic experience.»

<p align="center">
  <strong>VelyStream</strong> — Stream. Discover. Enjoy.
</p>---

✨ About VelyStream

VelyStream adalah aplikasi streaming anime Android yang dirancang dengan fokus pada pengalaman menonton yang simple, modern, cepat, dan nyaman.

VelyStream menggunakan VelyDocs API sebagai sumber data anime dan menyediakan berbagai fitur untuk membuat pengalaman streaming terasa lebih praktis.

🎯 Filosofi

«Less clutter. More anime.»

Tidak ada tampilan yang berlebihan. VelyStream dibuat supaya pengguna bisa menemukan anime, membuka detail, memilih episode, dan langsung menonton dengan pengalaman yang sederhana.

---

🚀 Features

- 🏠 Modern Home
  
  - Anime terbaru
  - Anime populer
  - Rekomendasi
  - Tampilan cinematic

- 🔎 Anime Search
  
  - Cari anime dengan cepat
  - Hasil pencarian terintegrasi dengan VelyDocs API

- 📖 Anime Details
  
  - Poster & thumbnail
  - Judul anime
  - Sinopsis
  - Informasi episode
  - Daftar episode

- ▶️ Streaming Player
  
  - Custom video player
  - Skip ±5 detik
  - Progress video
  - Episode navigation
  - Kontrol player yang minimal dan clean

- ❤️ Bookmark / Saved
  
  - Simpan anime favorit
  - Akses kembali anime dengan mudah

- 🕐 Watch History
  
  - Menyimpan anime yang pernah ditonton
  - Menyimpan episode terakhir
  - Menyimpan posisi/progress tontonan
  - Melanjutkan dari posisi terakhir

- 🔔 Anime Update Notification
  
  - Notifikasi ketika anime mendapatkan episode baru
  - Backend dapat memantau update secara berkala
  - Mendukung sistem subscription per anime

- 🔄 App Update System
  
  - Mengecek versi terbaru aplikasi
  - Memberikan pemberitahuan ketika update tersedia
  - Mendukung optional update maupun force update

---

🛠️ Technology

VelyStream dibangun dengan pendekatan native Android dan menggunakan beberapa komponen berikut:

Component| Usage
Android| Mobile application
Java / Android SDK| Application development
VelyDocs API| Anime data & API
Supabase| Backend, database & update monitoring
Firebase FCM| Push notification
GitHub Releases| APK distribution

---

🌐 VelyDocs API

VelyStream menggunakan VelyDocs API untuk mengambil data anime.

API menangani kebutuhan seperti:

- Anime listing
- Anime details
- Episode information
- Recent updates
- Streaming information

VelyDocs menjadi layer API antara VelyStream dan sumber data anime.

---

🔔 Update Notification Architecture

Sistem notifikasi update anime dapat berjalan walaupun aplikasi sedang tidak dibuka.

VelyDocs API
     │
     ▼
Supabase Scheduler
     │
     ▼
Supabase Edge Function
     │
     ├── Check latest episodes
     ├── Compare database state
     └── Prevent duplicate notification
     │
     ▼
Firebase FCM
     │
     ▼
VelyStream Android
     │
     ▼
🔔 New Episode

Dengan pendekatan ini, pengecekan update tidak bergantung pada aplikasi Android yang sedang terbuka.

---

📱 App Update System

VelyStream juga dapat menggunakan remote version checking.

VelyStream v1
      │
      ▼
Check Supabase
      │
      ▼
New version available?
      │
      ├── No → Continue
      │
      └── Yes
           │
           ▼
      Update Dialog
           │
           ▼
      GitHub Release
           │
           ▼
      Install VelyStream v2

Data seperti bookmark dan history dapat dipertahankan selama package name dan signing key aplikasi tetap sama.

---

🎨 Design

VelyStream menggunakan pendekatan desain:

- Minimal
- Modern
- Cinematic
- Clean
- Dark-focused
- Smooth navigation
- Fokus pada artwork anime

Inspirasi desain mengambil pendekatan aplikasi streaming modern dengan penyesuaian identitas VelyStream.

---

📦 Distribution

APK VelyStream didistribusikan melalui GitHub Releases.

Setiap versi memiliki release tersendiri:

Releases
│
├── v2.0.0
│   └── VelyStream-v2.0.0.apk
│
├── v1.1.0
│   └── VelyStream-v1.1.0.apk
│
└── v1.0.0
    └── VelyStream-v1.0.0.apk

---

🔐 Security

API key yang bersifat rahasia tidak seharusnya ditanam langsung di APK.

Untuk backend, secret dapat disimpan pada environment/secret storage sehingga tidak perlu diekspos kepada client.

«Never expose private API keys inside the Android application.»

---

📋 Requirements

Untuk menjalankan project dari source:

- Android Studio / Android development environment
- Android SDK
- Java / Gradle
- VelyDocs API access
- Supabase project jika menggunakan backend notification
- Firebase project jika menggunakan FCM

---

🧩 Project Structure

VelyStream/
│
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   ├── res/
│   │   │   └── AndroidManifest.xml
│   │   │
│   │   └── ...
│   │
│   └── build.gradle
│
├── gradle/
├── build.gradle
├── settings.gradle
└── README.md

---

🗺️ Roadmap

Current

- [x] Anime browsing
- [x] Anime search
- [x] Anime details
- [x] Episode list
- [x] Streaming
- [x] Bookmark
- [x] Watch history
- [x] Watch progress

Planned

- [ ] Per-anime notification subscription
- [ ] Improved streaming resolver
- [ ] Better recommendation system
- [ ] More player customization
- [ ] Performance improvements
- [ ] Automatic app update detection
- [ ] More streaming sources

---

⚠️ Disclaimer

VelyStream is an independent application and is not affiliated with or endorsed by any anime studio, distributor, or streaming platform.

VelyStream itself does not claim ownership of third-party anime content.

The application relies on external APIs and streaming sources. Availability and functionality may change depending on those external services.

---

👨‍💻 Creator

VelyStream
Created by Gxyenn

«Built with passion for anime and better mobile streaming.»

---

⭐ Support

If you like VelyStream, consider giving the repository a ⭐ on GitHub.

VelyStream — Your anime, your way. 🎬
