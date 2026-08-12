# Apollon Linux — Web Sitesi

Bu klasör, Apollon Linux'un resmi tanıtım web sitesini içerir.

## Dosya Yapısı

```
Apollon-Linux-web/
├── index.html         — Ana sayfa (tek sayfa, tüm bölümler)
├── style.css          — CSS tasarım sistemi (dark theme)
├── apollon-logo.png   — Apollon Linux logosu
└── README.md          — Bu dosya
```

## Bölümler

- **Hero**: Logo, başlık, indirme butonu, proje meta bilgileri
- **Özellikler**: 6 temel güvenlik özelliği (Tor, AppArmor, LUKS, Firejail, Firewall, Kernel Hardening)
- **Güvenlik Mimarisi**: 4 katmanlı güvenlik yapısı
- **Yazılımlar**: Önceden yüklü gelen güvenlik ve masaüstü araçları
- **Sistem Gereksinimleri**: CPU, RAM, Depolama, Boot bilgileri
- **İndir**: ISO indirme alanı, SHA256 checksum

## Yerel Geliştirme

```bash
# Tarayıcıda doğrudan açın
xdg-open index.html

# Veya Python HTTP sunucusu ile
python3 -m http.server 8080
# http://localhost:8080 adresini ziyaret edin
```

## Lisans

GPLv3 — Apollon Security Project
