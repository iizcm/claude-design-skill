# claude-design-skill

<div align="center">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
  <img src="https://img.shields.io/badge/Universal_AI_Agent_Skill-orange?style=for-the-badge" alt="Universal AI Agent Skill">
  <img src="https://img.shields.io/badge/Category-design-purple?style=for-the-badge" alt="Category: design">
</div>

## English

### Overview
The `claude-design` skill helps AI agents perform design work, specifically creating one-off HTML artifacts such as landing pages, interactive prototypes, presentation decks, and component explorations. It focuses on mimicking the design process and aesthetic judgment of a skilled designer, even in CLI/API environments where traditional graphical UI tools are unavailable. This skill emphasizes thoughtful composition, design system principles, and contextual awareness to avoid generic or "AI-slop" designs.

### When to Use
Use this skill when the task involves:
*   Creating a new design from scratch (e.g., a landing page, prototype, or deck).
*   Developing visual options or component explorations.
*   Designing onboarding flows, dashboards, or interactive mockups.
*   Redesigning based on provided screenshots, repositories, or brand documentation.
*   Any design task requiring a local HTML file as the deliverable, with a focus on good design principles.

**Avoid** using this for pure `DESIGN.md` token authoring (use `design-md` instead) or if the user explicitly asks for a design based on a known brand's existing system (consider `popular-web-designs`).

### Quick Start

1.  **Understand the Brief**: Clarify what is being designed, for whom, the desired artifact, and any constraints.
2.  **Gather Context**: Inspect provided documents, screenshots, repository files, or design assets to understand the visual vocabulary.
3.  **Commit to a Surface Archetype**: Before any visual tokens, decide on one of the seven surface archetypes (Monitor, Operate, Compare, Configure, Decide/Learn, Explore, Command/Inspect) to guide composition.
4.  **Define the Design System**: Establish colors, typography, spacing, radii, shadows, motion posture, component treatment, and interaction rules for the artifact.
5.  **Choose the Right Format**: Determine if the output should be a static comparison, interactive prototype, slide deck, component lab, or motion study.
6.  **Build the Artifact**: Prefer a single, self-contained HTML file with embedded CSS and JavaScript for portability.
7.  **Verify**: Confirm file existence, check for syntax issues, and if possible, open in a browser tool to check for console errors or visual fidelity.
8.  **Report**: Provide the exact file path, what was created, verification status, and any next steps.

### Key Features and Workflow

#### Design Principles
*   **Start From Context, Not Vibes**: Prioritize understanding existing brand guidelines, components, and user needs over generic aesthetic choices.
*   **Surface-First Composition**: Explicitly choose a surface archetype (Monitor, Operate, Compare, Configure, Decide/Learn, Explore, Command/Inspect) before defining visual tokens to ensure appropriate layout and hierarchy.
*   **Content Discipline**: Avoid filler content. Every element must serve a purpose.
*   **Anti-Slop Rules**: Guard against common "AI design sludge" such as aggressive gradients, glassmorphism, generic icons, and uninspired layouts.

#### Workflow Steps (Detailed)
1.  **Understand the brief**: What, who, what artifact, constraints.
2.  **Gather context**: Read docs, screenshots, repo files.
3.  **Commit to a surface**: Name the archetype (e.g., "This is a **Monitor** surface, so density and glanceability beat a hero").
4.  **Define the design system**: Colors, type, spacing, etc.
5.  **Choose the right format**: Static HTML, prototipe interaktif, presentasi slide.
6.  **Build the artifact**: Pilih HTML yang berdiri sendiri, simpan versi sebelumnya untuk revisi.
7.  **Verifikasi**: Periksa keberadaan file, sintaksis, kesalahan browser, dan lakukan audit diri "Diagnostik Slop".
8.  **Laporkan secara singkat**: Jalur file, konten, verifikasi, tindakan selanjutnya.

#### Artifact Format
*   **HTML Mandiri**: Gunakan nama file deskriptif (`Landing Page.html`), sematkan CSS di `<style>` dan JS di `<script>`, hindari dependensi jarak jauh kecuali penting.
*   **Revisi**: Simpan sebagai `Nama v2.html`, `Nama v3.html`, atau gunakan tombol di halaman untuk varian.
*   **Implementasi Repo**: Ikuti tumpukan yang ada, gunakan komponen/token dari repo.

#### Standar HTML/CSS/JS
*   Gunakan CSS modern: variabel, grid, kueri kontainer, `text-wrap: pretty`, status fokus/hover yang nyata, `prefers-reduced-motion`.
*   Hindari file monolitik besar, asumsi viewport yang rapuh, target klik kecil.
*   Target klik seluler: ≥44px. Teks cetak: ≥12pt. Teks presentasi slide: ≥24px untuk 1920x1080.

#### Panduan React
*   Gunakan HTML/CSS/JS biasa secara default. React hanya untuk status yang bermakna, varian komponen, atau interaksi yang kompleks.
*   Jika menggunakan React dari CDN di HTML mandiri, pin versi yang tepat, hindari URL yang tidak dipin dan `type="module"` kecuali diperlukan.

#### Aturan Presentasi
*   Kanvas ukuran tetap (default 1920×1080, 16:9).
*   Navigasi keyboard, jumlah slide yang terlihat, persistensi `localStorage` untuk slide saat ini.
*   Slide jarang, maksimal 1-2 warna latar belakang.

#### Aturan Prototipe
*   Jalur utama yang dapat diklik, penyertaan status kunci (default, hover, loading, error).
*   Kontrol di halaman untuk variasi, persistensi `localStorage` untuk status penting.

#### Aturan Variasi
*   Secara default setidaknya tiga opsi: Konservatif, Kuat, Divergen.
*   Variasi dapat mengeksplorasi tata letak, hierarki, skala jenis, kepadatan, warna, gerakan, model interaksi.

#### Desain yang Dapat Diubah (Mode CLI/API)
*   Tambahkan kontrol di halaman yang disebut `Tweaks` untuk tema, tata letak, kepadatan, warna aksen, dll.
*   Biarkan `Tweaks` tidak mencolok; simpan nilai dengan `localStorage`.

#### Diagnostik Slop (Audit Diri)
Nilai desain dari 10 untuk "endapan desain AI" menggunakan 10 tanda khusus (misalnya, "Gradien teknologi", "Warna teknologi generik", "Kisi fitur", "Permukaan salah"). Diagnosis terlebih dahulu, lalu obati berdasarkan skor (tata ulang untuk masalah komposisi, warnai ulang/jenis ulang untuk masalah estetika, hapus dekorasi untuk elemen yang tidak perlu).

### Pitfalls
*   Avoid pasting hosted tool schemas.
*   Do not over-ask or under-ask for details; context is key.
*   Do not produce generic SaaS layouts.
*   Do not claim browser verification without actual verification.

## Bahasa Indonesia

### Gambaran Umum
Skill `claude-design` membantu agen AI melakukan pekerjaan desain, khususnya membuat artefak HTML sekali pakai seperti landing page, prototipe interaktif, presentasi, dan eksplorasi komponen. Skill ini berfokus pada meniru proses desain dan penilaian estetika dari desainer terampil, bahkan di lingkungan CLI/API di mana alat UI grafis tradisional tidak tersedia. Skill ini menekankan komposisi yang cermat, prinsip-prinsip sistem desain, dan kesadaran kontekstual untuk menghindari desain yang generik atau "AI-slop".

### Kapan Menggunakan
Gunakan skill ini ketika tugas melibatkan:
*   Membuat desain baru dari awal (misalnya, landing page, prototipe, atau presentasi).
*   Mengembangkan opsi visual atau eksplorasi komponen.
*   Mendesain alur onboarding, dashboard, atau mockup interaktif.
*   Mendesain ulang berdasarkan tangkapan layar, repositori, atau dokumentasi merek yang disediakan.
*   Tugas desain apa pun yang memerlukan file HTML lokal sebagai hasil akhir, dengan fokus pada prinsip desain yang baik.

**Hindari** menggunakan ini untuk penulisan token `DESIGN.md` murni (gunakan `design-md` sebagai gantinya) atau jika pengguna secara eksplisit meminta desain berdasarkan sistem merek yang dikenal (pertimbangkan `popular-web-designs`).

### Mulai Cepat

1.  **Pahami Brief**: Klarifikasi apa yang sedang dirancang, untuk siapa, artefak yang diinginkan, dan batasan apa pun.
2.  **Kumpulkan Konteks**: Periksa dokumen, tangkapan layar, file repositori, atau aset desain yang disediakan untuk memahami kosakata visual.
3.  **Tentukan Arketipe Permukaan**: Sebelum token visual apa pun, putuskan salah satu dari tujuh arketipe permukaan (Monitor, Operate, Compare, Configure, Decide/Learn, Explore, Command/Inspect) untuk memandu komposisi.
4.  **Definisikan Sistem Desain**: Tetapkan warna, tipografi, jarak, radius, bayangan, postur gerakan, perlakuan komponen, dan aturan interaksi untuk artefak.
5.  **Pilih Format yang Tepat**: Tentukan apakah output harus berupa perbandingan statis, prototipe interaktif, presentasi slide, lab komponen, atau studi gerakan.
6.  **Bangun Artefak**: Pilih file HTML tunggal yang berdiri sendiri dengan CSS dan JavaScript tersemat untuk portabilitas.
7.  **Verifikasi**: Konfirmasikan keberadaan file, periksa masalah sintaksis, dan jika memungkinkan, buka di alat browser untuk memeriksa kesalahan konsol atau fidelitas visual.
8.  **Laporkan**: Berikan jalur file yang tepat, apa yang dibuat, status verifikasi, dan langkah selanjutnya.

### Fitur Utama dan Alur Kerja

#### Prinsip Desain
*   **Mulai dari Konteks, Bukan Hanya Estetika**: Prioritaskan pemahaman pedoman merek, komponen, dan kebutuhan pengguna yang ada di atas pilihan estetika generik.
*   **Komposisi Berbasis Permukaan**: Secara eksplisit pilih arketipe permukaan (Monitor, Operate, Compare, Configure, Decide/Learn, Explore, Command/Inspect) sebelum mendefinisikan token visual untuk memastikan tata letak dan hierarki yang sesuai.
*   **Disiplin Konten**: Hindari konten pengisi. Setiap elemen harus memiliki tujuan.
*   **Aturan Anti-Slop**: Waspadai "endapan desain AI" umum seperti gradien agresif, glassmorphism, ikon generik, dan tata letak yang tidak terinspirasi.

#### Langkah-langkah Alur Kerja (Rinci)
1.  **Pahami brief**: Apa, siapa, artefak apa, batasan.
2.  **Kumpulkan konteks**: Baca dokumen, tangkapan layar, file repo.
3.  **Tentukan permukaan**: Sebutkan arketipe (misalnya, "Ini adalah permukaan **Monitor**, jadi kepadatan dan kemampuan untuk melihat sekilas mengalahkan hero").
4.  **Definisikan sistem desain**: Warna, jenis, spasi, dll.
5.  **Pilih format yang tepat**: Static HTML, prototipe interaktif, presentasi slide.
6.  **Bangun artefak**: Pilih HTML yang berdiri sendiri, simpan versi sebelumnya untuk revisi.
7.  **Verifikasi**: Periksa keberadaan file, sintaksis, kesalahan browser, dan lakukan audit diri "Diagnostik Slop".
8.  **Laporkan secara singkat**: Jalur file, konten, verifikasi, tindakan selanjutnya.

#### Format Artefak
*   **HTML Mandiri**: Gunakan nama file deskriptif (`Landing Page.html`), sematkan CSS di `<style>` dan JS di `<script>`, hindari dependensi jarak jauh kecuali penting.
*   **Revisi**: Simpan sebagai `Nama v2.html`, `Nama v3.html`, atau gunakan tombol di halaman untuk varian.
*   **Implementasi Repo**: Ikuti tumpukan yang ada, gunakan komponen/token dari repo.

#### Standar HTML/CSS/JS
*   Gunakan CSS modern: variabel, grid, kueri kontainer, `text-wrap: pretty`, status fokus/hover yang nyata, `prefers-reduced-motion`.
*   Hindari file monolitik besar, asumsi viewport yang rapuh, target klik kecil.
*   Target klik seluler: ≥44px. Teks cetak: ≥12pt. Teks presentasi slide: ≥24px untuk 1920x1080.

#### Panduan React
*   Gunakan HTML/CSS/JS biasa secara default. React hanya untuk status yang bermakna, varian komponen, atau interaksi yang kompleks.
*   Jika menggunakan React dari CDN di HTML mandiri, pin versi yang tepat, hindari URL yang tidak dipin dan `type="module"` kecuali diperlukan.

#### Aturan Presentasi
*   Kanvas ukuran tetap (default 1920×1080, 16:9).
*   Navigasi keyboard, jumlah slide yang terlihat, persistensi `localStorage` untuk slide saat ini.
*   Slide jarang, maksimal 1-2 warna latar belakang.

#### Aturan Prototipe
*   Jalur utama yang dapat diklik, penyertaan status kunci (default, hover, loading, error).
*   Kontrol di halaman untuk variasi, persistensi `localStorage` untuk status penting.

#### Aturan Variasi
*   Secara default setidaknya tiga opsi: Konservatif, Kuat, Divergen.
*   Variasi dapat mengeksplorasi tata letak, hierarki, skala jenis, kepadatan, warna, gerakan, model interaksi.

#### Desain yang Dapat Diubah (Mode CLI/API)
*   Tambahkan kontrol di halaman yang disebut `Tweaks` untuk tema, tata letak, kepadatan, warna aksen, dll.
*   Biarkan `Tweaks` tidak mencolok; simpan nilai dengan `localStorage`.

#### Diagnostik Slop (Audit Diri)
Nilai desain dari 10 untuk "endapan desain AI" menggunakan 10 tanda khusus (misalnya, "Gradien teknologi", "Warna teknologi generik", "Kisi fitur", "Permukaan salah"). Diagnosis terlebih dahulu, lalu obati berdasarkan skor (tata ulang untuk masalah komposisi, warnai ulang/jenis ulang untuk masalah estetika, hapus dekorasi untuk elemen yang tidak perlu).

### Jebakan
*   Hindari menempel skema alat yang dihosting.
*   Jangan terlalu banyak bertanya atau terlalu sedikit bertanya tentang detail; konteks adalah kunci.
*   Jangan menghasilkan tata letak SaaS generik.
*   Jangan mengklaim verifikasi browser tanpa verifikasi yang sebenarnya.
