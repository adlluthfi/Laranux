# 🐧 Laranux - Linux Development Stack Manager

<p align="center">
  <img src="laranux.png" alt="Laranux Logo" width="200"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/platform-Linux-orange.svg" alt="Platform">
  <img src="https://img.shields.io/badge/version-1.0.0-green.svg" alt="Version">
  <img src="https://img.shields.io/badge/status-stable-brightgreen.svg" alt="Status">
</p>

<p align="center">
  <strong>Kelola Stack Development Linux Anda dengan Mudah!</strong><br>
  Alternatif Laragon untuk Linux - Manage Nginx, Apache, MariaDB, PostgreSQL, Redis, dan PHP-FPM dengan GUI yang Modern.
</p>

<p align="center">
  <a href="#-download">Download</a> •
  <a href="#-fitur-unggulan">Fitur</a> •
  <a href="#-instalasi">Instalasi</a> •
  <a href="#-cara-pakai">Cara Pakai</a> •
  <a href="#-faq">FAQ</a>
</p>

---

## 🎯 Tentang Laranux

**Laranux** adalah aplikasi GUI modern untuk Linux yang memudahkan developer web mengelola web server stack mereka. Terinspirasi dari **Laragon** (Windows), Laranux menyediakan interface yang intuitif untuk mengontrol services seperti Nginx, Apache, MariaDB, PostgreSQL, Redis, dan PHP-FPM.

### 💡 Kenapa Laranux?

- ⚡ **Cepat & Ringan** - Interface Qt native yang responsive
- 🎨 **Modern UI** - Design yang clean dan user-friendly
- 🔧 **Powerful** - 9 services supported dengan version switcher
- 🚀 **Produktif** - Quick installer untuk WordPress, Laravel, CodeIgniter
- 🌐 **Auto Virtual Hosts** - Project `.test` domain otomatis
- 🔒 **Auto HTTPS** - Self-signed SSL certificate generation
- 💯 **100% Linux** - Didesain khusus untuk ekosistem Linux

---

## 📥 Download

### Latest Release: v1.0.0

**Download untuk distribusi Anda:**

| Distribusi | Package | Download |
|------------|---------|----------|
| **Ubuntu/Debian** | `.deb` | [Download](https://github.com/adlluthfi/Laranux/releases/latest/download/laranux_1.0.0_amd64.deb) |
| **Fedora/RHEL** | `.rpm` | [Download](https://github.com/adlluthfi/Laranux/releases/latest/download/laranux-1.0.0.x86_64.rpm) |
| **Arch Linux** | `.pkg.tar.zst` | [Download](https://github.com/adlluthfi/Laranux/releases/latest/download/laranux-1.0.0-1-x86_64.pkg.tar.zst) |
| **Universal** | `.tar.gz` | [Download](https://github.com/adlluthfi/Laranux/releases/latest/download/laranux-1.0.0-linux-x86_64.tar.gz) |

> **Catatan:** Link download akan aktif setelah release pertama di-publish.

### System Requirements

- **OS:** Linux dengan systemd (Ubuntu 20.04+, Fedora 34+, Arch, dll)
- **RAM:** Minimal 512 MB
- **Disk:** 50 MB free space
- **Dependencies:** Qt5 atau Qt6 libraries

---

## 🖥️ Sistem Operasi yang Didukung

### ✅ **Compatible (Berjalan dengan baik):**

**Linux Distributions:**
- Ubuntu / Debian / Linux Mint
- Fedora / Red Hat / CentOS
- Arch Linux / Manjaro
- openSUSE
- Pop!_OS
- Zorin OS
- Elementary OS
- Dan semua distro Linux dengan **systemd**

### ❌ **Tidak Compatible:**

**Windows:**
- ❌ Tidak ada `systemctl` (menggunakan Windows Services)
- ❌ Service management berbeda
- ❌ Path structure berbeda (`C:\` vs `/`)

**macOS:**
- ❌ Tidak ada `systemctl` (menggunakan `launchctl`)
- ❌ Service management berbeda (brew services)

**BSD (FreeBSD, OpenBSD):**
- ❌ Service management berbeda (`rc.d`)
- ❌ Tidak menggunakan systemd

> **Catatan:** Laranux adalah aplikasi **khusus Linux** yang menggunakan systemctl, pkexec, dan systemd service management. Mirip seperti Laragon yang khusus untuk Windows, Laranux didesain khusus untuk ekosistem Linux.

---

## ✨ Fitur Unggulan

<table>
<tr>
<td width="50%">

### 🎛️ Service Management
- ✅ **9 Services Support**
  - Nginx & Apache2
  - MariaDB & MySQL
  - PostgreSQL & MongoDB
  - Redis & Memcached
  - PHP-FPM
- 🚦 **Real-time Monitor** (update 2s)
- ⚡ **Start/Stop/Restart** semua atau individual
- 🔀 **Version Switcher** (PHP, Python, Node.js)

</td>
<td width="50%">

### 🚀 Developer Tools
- 📦 **Quick Installer**
  - WordPress
  - Laravel
  - CodeIgniter
- 🌐 **Auto Virtual Hosts** (`.test` domain)
- 🔒 **Auto HTTPS** (SSL generation)
- 📝 **Config Editor** (1-click access)

</td>
</tr>
</table>

### 💼 Productivity Features
- 📁 **Quick Access** - Buka root folder, localhost, terminal dengan 1 klik
- 🎨 **Modern UI** - Interface 1920x1200 yang responsive
- ⚙️ **Settings** - Auto-detect services & port configuration
- 🔧 **Fix Permissions** - Auto-fix `/var/www/html` permissions

---

## 📋 Prasyarat

Sebelum install Laranux, pastikan services yang ingin Anda kelola sudah terinstall:

### Instalasi Services (Opsional)

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install nginx apache2 mariadb-server mysql-server \
                 postgresql mongodb-org redis-server memcached \
                 php-fpm php-mysql php-pgsql

# Fedora/RHEL
sudo dnf install nginx httpd mariadb-server mysql-server \
                 postgresql mongodb redis memcached \
                 php-fpm php-mysqlnd php-pgsql

# Arch Linux
sudo pacman -S nginx apache mariadb mysql postgresql \
               mongodb redis memcached php php-fpm
```

> **Tip:** Anda tidak perlu install semua services. Laranux hanya akan menampilkan services yang terdeteksi di sistem Anda.

---

---

## 🚀 Instalasi

### Metode 1: Package Manager (Recommended)

#### Ubuntu/Debian (.deb)
```bash
# Download package
wget https://github.com/adlluthfi/Laranux/releases/latest/download/laranux_1.0.0_amd64.deb

# Install
sudo dpkg -i laranux_1.0.0_amd64.deb
sudo apt-get install -f  # Fix dependencies jika ada

# Jalankan
Laranux
```

#### Fedora/RHEL (.rpm)
```bash
# Download package
wget https://github.com/adlluthfi/Laranux/releases/latest/download/laranux-1.0.0.x86_64.rpm

# Install
sudo dnf install ./laranux-1.0.0.x86_64.rpm

# Atau dengan rpm
sudo rpm -ivh laranux-1.0.0.x86_64.rpm

# Jalankan
Laranux
```

#### Arch Linux
```bash
# Download package
wget https://github.com/adlluthfi/Laranux/releases/latest/download/laranux-1.0.0-1-x86_64.pkg.tar.zst

# Install
sudo pacman -U laranux-1.0.0-1-x86_64.pkg.tar.zst

# Jalankan
Laranux
```

### Metode 2: Universal Binary (.tar.gz)

Untuk distribusi Linux lainnya:

```bash
# Download
wget https://github.com/adlluthfi/Laranux/releases/latest/download/laranux-1.0.0-linux-x86_64.tar.gz

# Extract
tar -xzf laranux-1.0.0-linux-x86_64.tar.gz
cd laranux-1.0.0

# Install
sudo ./install.sh

# Jalankan
Laranux
```

### Lokasi Instalasi

Setelah instalasi, file berada di:
- 📦 **Binary:** `/usr/local/bin/Laranux`
- 🖼️ **Icon:** `/usr/local/share/pixmaps/laranux.png`
- 🗂️ **Desktop Entry:** `/usr/share/applications/laranux.desktop`

### Cara Menjalankan

1. **Dari Application Launcher:**
   - Tekan `Super`/`Windows` key
   - Ketik "Laranux"
   - Klik icon Laranux

2. **Dari Terminal:**
   ```bash
   Laranux
   ```

3. **Dari Menu:**
   - Applications → Development → Laranux

---

---

## 📖 Cara Pakai

### Quick Start

1. **Buka Laranux** dari application launcher atau ketik `Laranux` di terminal

2. **Start Services**
   - Klik tombol **"Start All"** untuk menjalankan semua services
   - Atau gunakan toggle switch untuk individual service

3. **Monitor Status**
   - Status otomatis update setiap 2 detik
   - 🟢 Hijau = Service running
   - 🔴 Merah = Service stopped

### Fitur-Fitur Utama

#### 🎛️ Service Control
- **Start All / Stop All** - Kontrol semua services sekaligus
- **Individual Toggle** - Start/stop service tertentu
- **Context Menu** - Klik kanan untuk switch version (PHP, Python, Node.js)

#### 🚀 Quick App Installer
1. Klik tombol **"Create Project"**
2. Pilih aplikasi: WordPress, Laravel, atau CodeIgniter
3. Masukkan nama project
4. Laranux akan:
   - Download & install aplikasi
   - Buat database otomatis
   - Setup virtual host `.test`
   - Generate SSL certificate
   - Buka browser ke project

#### 🌐 Virtual Hosts
- Otomatis detect project di `/var/www/html`
- Auto-create domain `.test` (contoh: `myproject.test`)
- Support HTTPS dengan self-signed certificate
- Edit `/etc/hosts` otomatis

#### 📝 Config Editor
- Klik **"Edit Configs"** untuk akses cepat:
  - `php.ini` - PHP configuration
  - `nginx.conf` - Nginx configuration
  - `apache2.conf` - Apache configuration
  - `my.cnf` - MySQL/MariaDB configuration
  - `/etc/hosts` - Hosts file

#### 📁 Quick Access
- **Open Localhost** - Buka `http://localhost` di browser
- **Open Root** - Buka `/var/www/html` di file manager
- **Open Terminal** - Buka terminal di `/var/www/html`
- **Fix Permissions** - Auto-fix ownership `/var/www/html`

#### ⚙️ Settings
- Auto-detect installed services
- Enable/disable services yang ditampilkan
- Konfigurasi custom port untuk setiap service

---

## ❓ FAQ

<details>
<summary><strong>Q: Laranux tidak bisa start services?</strong></summary>

**A:** Pastikan:
1. Services sudah terinstall di sistem
2. PolicyKit (`policykit-1`) sudah terinstall
3. User Anda punya akses sudo
4. Cek status manual: `sudo systemctl status nginx`
</details>

<details>
<summary><strong>Q: Window icon tidak muncul di title bar?</strong></summary>

**A:** Di GNOME 40+, window icon tidak ditampilkan by default. Untuk enable:
```bash
gsettings set org.gnome.desktop.wm.preferences button-layout 'icon:minimize,maximize,close'
```
Atau buka GNOME Tweaks → Windows → Titlebar Buttons
</details>

<details>
<summary><strong>Q: Permission denied saat akses /var/www/html?</strong></summary>

**A:** Klik tombol **"Fix Permissions"** di Laranux, atau jalankan manual:
```bash
sudo chown -R $USER:$USER /var/www/html
sudo chmod -R 755 /var/www/html
```
</details>

<details>
<summary><strong>Q: Virtual host .test tidak bisa diakses?</strong></summary>

**A:** Pastikan:
1. Entry sudah ada di `/etc/hosts`
2. Nginx/Apache sudah restart
3. Browser sudah clear cache
4. Akses dengan `https://` (bukan `http://`)
</details>

<details>
<summary><strong>Q: Cara uninstall Laranux?</strong></summary>

**A:** 
```bash
# Ubuntu/Debian
sudo apt remove laranux

# Fedora/RHEL
sudo dnf remove laranux

# Arch
sudo pacman -R laranux

# Manual
sudo rm /usr/local/bin/Laranux
sudo rm /usr/local/share/pixmaps/laranux.png
sudo rm /usr/share/applications/laranux.desktop
```
</details>

<details>
<summary><strong>Q: Apakah Laranux bisa di Windows/macOS?</strong></summary>

**A:** Tidak. Laranux didesain khusus untuk Linux dengan systemd. Untuk Windows, gunakan [Laragon](https://laragon.org/).
</details>

---

---

## 📸 Screenshots

> Screenshots akan ditambahkan segera...

---

## 🔄 Update

Untuk update ke versi terbaru:

```bash
# Ubuntu/Debian
sudo apt update
sudo apt upgrade laranux

# Fedora/RHEL
sudo dnf upgrade laranux

# Arch
sudo pacman -Syu laranux

# Manual
# Download package terbaru dari releases dan install ulang
```

---

## 🐛 Laporkan Bug

Menemukan bug atau punya saran? Silakan buka [Issue](https://github.com/adlluthfi/Laranux/issues) di GitHub.

**Template Issue:**
```
**Deskripsi Bug:**
[Jelaskan bug yang terjadi]

**Langkah Reproduksi:**
1. Buka Laranux
2. Klik ...
3. Lihat error ...

**Expected Behavior:**
[Apa yang seharusnya terjadi]

**Screenshots:**
[Jika ada]

**System Info:**
- OS: Ubuntu 22.04
- Laranux Version: 1.0.0
- Services: Nginx, MariaDB, PHP 8.1
```

---

## 📄 Lisensi

Laranux dirilis di bawah [MIT License](LICENSE).

```
Copyright (c) 2026 Luthfi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 👨‍💻 Author

**Luthfi**

- 🌐 GitHub: [@adlluthfi](https://github.com/adlluthfi)
- 📧 Email: adlluthfi@gmail.com

---

## 🙏 Acknowledgments

- 💡 Terinspirasi dari [Laragon](https://laragon.org/) untuk Windows
- 🛠️ Dibangun dengan [Qt Framework](https://www.qt.io/)
- 🎨 Icon: Custom design
- 🐧 Untuk komunitas Linux developer di seluruh dunia

---

## ⭐ Support

Jika Laranux membantu Anda, silakan:
- ⭐ **Star** repository ini di GitHub
- 🐛 **Laporkan bug** atau request fitur
- 📢 **Share** ke developer lain
- ☕ **Donate** untuk support development

---

## 🔗 Links

- 📦 [Releases](https://github.com/adlluthfi/Laranux/releases)
- 🐛 [Issues](https://github.com/adlluthfi/Laranux/issues)
- 📖 [Wiki](https://github.com/adlluthfi/Laranux/wiki)
- 💬 [Discussions](https://github.com/adlluthfi/Laranux/discussions)

---

<p align="center">
  Made with ❤️ for Linux Developers<br>
  <strong>Laranux - Your Linux Development Stack Manager</strong>
</p>
