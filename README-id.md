# git-cal

[English](README.md) | [Bahasa Indonesia](README-id.md)

---

git-cal adalah alat sederhana untuk melihat kalender kontribusi Git Anda langsung di terminal, mirip dengan grafik kontribusi di profil GitHub.

![Tangkapan Layar Kalender Git](screenshots/Screenshot%202026-08-17%20224645.png)

### Fitur Modern
Alat ini telah diperbarui agar berfungsi dengan repositori lama dan workspace modern:
- **Pemindaian Otomatis Workspace**: Tunjuk ke folder root, dan skrip akan otomatis menemukan serta menggabungkan data dari semua repositori Git di dalamnya.
- **Penjelajah Waktu**: Lihat riwayat kontribusi dari tahun atau periode mana pun menggunakan opsi `--since` dan `--anchor`.
- **Tampilan Agregat**: Gabungkan riwayat dari banyak repositori ke dalam satu tampilan kalender.
- **Lintas Platform**: Mendukung Linux, macOS, dan Windows.

---

### Prasyarat & Instalasi

`git-cal` membutuhkan **Perl** dan **Git**.

#### Linux
Perl biasanya sudah terpasang di sebagian besar distribusi Linux.
```bash
# Ubuntu / Debian
sudo apt update && sudo apt install perl git

# Arch Linux
sudo pacman -S perl git

# Jadikan git-cal dapat dieksekusi
chmod +x git-cal
```

#### macOS
Perl dan Git tersedia melalui macOS Command Line Tools atau Homebrew:
```bash
# Opsional: Instal melalui Homebrew
brew install perl git

# Jadikan git-cal dapat dieksekusi
chmod +x git-cal
```

#### Windows
Ada tiga opsi untuk menjalankan `git-cal` di Windows:

- **Opsi 1: Git Bash (Direkomendasikan & Termudah)**
  Jika Anda memiliki **Git for Windows**, buka **Git Bash** di direktori proyek Anda. `perl` sudah termasuk otomatis di Git Bash!
  ```bash
  ./git-cal
  # atau
  perl git-cal
  ```

- **Opsi 2: Windows PowerShell / CMD**
  Jika `perl git-cal` di PowerShell memunculkan `'perl' is not recognized`, instal **Strawberry Perl**:
  ```powershell
  # Via Winget di PowerShell
  winget install StrawberryPerl.StrawberryPerl
  ```
  *Atau unduh installer secara manual dari [strawberryperl.com](https://strawberryperl.com/).*
  Setelah instalasi, restart PowerShell dan jalankan:
  ```powershell
  perl git-cal
  ```

- **Opsi 3: WSL (Windows Subsystem for Linux)**
  Jalankan langsung di dalam terminal distribusi Linux Anda di Windows:
  ```bash
  wsl ./git-cal
  ```

---

### Penggunaan

#### 1. Penggunaan Dasar
Jalankan di dalam repositori Git mana pun:
- **Linux / macOS / Git Bash:**
  ```bash
  ./git-cal
  ```
- **PowerShell / CMD:**
  ```powershell
  perl git-cal
  ```

#### 2. Pindai Seluruh Workspace
Tunjuk ke folder berisi banyak proyek Git untuk melihat aktivitas agregat:
```bash
# Linux / macOS / Git Bash
./git-cal "/path/ke/proyek-anda/"

# Windows PowerShell / CMD
perl git-cal "C:\path\ke\proyek-anda"
```

#### 3. Lihat Riwayat Masa Lalu (Penjelajah Waktu)
Lihat kontribusi dari periode masa lalu tertentu (misal tahun 2015):
```bash
./git-cal --since="15 years" --anchor="2015-12-31"
```

#### 4. Filter Berdasarkan Penulis
```bash
./git-cal --author="Nama Anda"
```

---

### Kredit dan Lisensi
Alat ini adalah versi modern dari proyek asli yang dibuat oleh:
- **Penulis Asli**: Karthik Katooru ([@k4rthik](https://github.com/k4rthik))
- **Lisensi**: MIT License

---

*[English](README.md)*
