<div align="center">

<img src="https://apoben.github.io/Apollon-Linux/apollon-logo.png" alt="Apollon Linux Logo" width="120" />

# 🛡️ Apollon Linux
**Gizliliğiniz için tasarlandı. Güvenliğiniz için güçlendirildi.**

[![Version](https://img.shields.io/badge/Version-v0.1_Pre--Alpha-gold.svg)](#)
[![Base](https://img.shields.io/badge/Base-Debian_13_(Trixie)-blue.svg)](https://debian.org)
[![License](https://img.shields.io/badge/License-GPLv3-green.svg)](#)
[![Website](https://img.shields.io/badge/Website-apoben.github.io%2FApollon--Linux-purple.svg)](https://apoben.github.io/Apollon-Linux/)

*Apollon Linux, Debian tabanlı, siber güvenlik, anonimlik ve tam gizlilik odaklı açık kaynaklı bir işletim sistemidir. Her katmanı agresif güvenlik politikalarıyla donatılmıştır.*

[ISO İndir](https://apoben.github.io/Apollon-Linux/) • [Özellikler](#-temel-özellikler) • [Derleme Rehberi](#-iso-imajını-derleme)
</div>

---

## 🔒 Güvenlik Mimarisi

Sıradan dağıtımların aksine Apollon Linux, kullanıcıyı dış ve iç tehditlere karşı korumak için çekirdek (kernel) seviyesinden ağ seviyesine kadar izole edilmiş bir mimari kullanır.

- **Kernel Sıkılaştırma:** Hardened boot parametreleri (Örn: `init_on_alloc=1`, `slab_nomerge`, `vsyscall=none`, `page_alloc.shuffle=1`) ile 0-day (sıfır gün) bellek zafiyetlerine karşı direnç.
- **Zorunlu Erişim Kontrolü:** AppArmor profilleri çekirdek düzeyinde aktiftir, uygulamaların sisteme erişimini sıkı bir şekilde kısıtlar.
- **İzole Edilmiş Uygulamalar:** Riskli veya dış ağa bağlanan uygulamalar **Firejail** ve **Bubblewrap** ile sandbox (kum havuzu) ortamına hapsedilir.
- **Disk Şifreleme:** Kurulum sırasında by-pass edilemeyen zorunlu LUKS2 (Linux Unified Key Setup) tam disk şifreleme.

## ✨ Temel Özellikler

| Özellik | Açıklama |
|---|---|
| **Tor Entegrasyonu** | Trafik analizlerine karşı koruma. Tor Browser varsayılan olarak yüklü gelir. |
| **Ağ Gizliliği** | UFW ve nftables tabanlı sıkılaştırılmış firewall. Macchanger ile donanım kimliği (MAC) maskeleme. |
| **Hafif & Şık Masaüstü** | Hızlı, minimal ve modern bir kullanıcı deneyimi sunan GNOME Wayland masaüstü ortamı. |
| **Gizlilik Araçları** | Metadata temizliği için MAT2, iz silici BleachBit, şifre kasası KeePassXC ve anonim dosya paylaşımı için OnionShare varsayılan olarak gelir. |

## ⚙️ Sistem Gereksinimleri

Optimum güvenlik ve performans deneyimi için önerilen donanım gereksinimleri:

- **İşlemci (CPU):** 64-bit (x86_64) mimarili modern işlemci
- **Bellek (RAM):** Minimum 2 GB (4 GB ve üzeri önerilir)
- **Depolama:** Minimum 20 GB boş disk alanı (LUKS2 şifrelemesi için tam performanslı SSD önerilir)
- **Firmware:** UEFI (Secure Boot uyumlu) veya Legacy BIOS

## 🛠️ ISO İmajını Derleme

Kendi güvenliğini kendi elleriyle oluşturmak isteyen kullanıcılar için Apollon Linux kaynak kodundan kolayca derlenebilir yapıdadır. Bir Debian veya Ubuntu ortamına ihtiyacınız vardır.

```bash
# 1. Depoyu klonlayın
git clone https://github.com/ApoBen/Apollon-Linux.git
cd Apollon-Linux

# 2. Gerekli derleme araçlarını ve bağımlılıkları yükleyin
make deps

# 3. Canlı sistem konfigürasyonunu oluşturun
make config

# 4. ISO imajını derlemeyi başlatın (İnternet hızınıza göre 30-60 dk sürebilir)
make build
```

Derleme tamamlandığında `apollon-linux-0.1-pre-alpha-exodus-amd64.iso` dosyası proje dizininde hazır olacaktır. 

## 🌐 Web Sitesi & İndirme

İşletim sistemimizin önizleme sürümünü indirmek, güncel duyuruları takip etmek ve projeyi incelemek için resmi sitemizi ziyaret edin:
👉 **[Apollon Linux Resmi Web Sitesi](https://apoben.github.io/Apollon-Linux/)**

## 📄 Lisans

Bu proje, açık kaynak felsefesine sıkı sıkıya bağlı kalarak **GPLv3** lisansı ile dağıtılmaktadır. Yazılımı kopyalamakta, değiştirmekte ve dağıtmakta özgürsünüz.
