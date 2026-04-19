# 🚀 MASTER PLAN – SahibindenKlon

> Türkiye'nin En Güçlü İlan Platformu | PHP 8.2 + MySQL 8.0 + Vanilla MVC

---

## 📋 Doküman Haritası

Tüm teknik detaylar `.claude/docs/` altında 5 dosyaya bölünmüştür.
**Ajanlar bu sırayla okumalı ve uygulamalıdır:**

| # | Dosya | İçerik | Satır |
|---|-------|--------|-------|
| 1 | [1-architecture.md](.claude/docs/1-architecture.md) | Tech stack, vizyon, klasör yapısı, Core MVC framework detayı | ~170 |
| 2 | [2-db-schema.md](.claude/docs/2-db-schema.md) | 13 tablo SQL şeması, seed data referansı, kategori attribute'ları | ~280 |
| 3 | [3-api-routes.md](.claude/docs/3-api-routes.md) | 60+ route tanımı (Public, Auth, İlan, Arama, Kategori, Mesaj, Admin) | ~130 |
| 4 | [4-frontend-components.md](.claude/docs/4-frontend-components.md) | CSS tokens, 8 UI komponent, sayfa tasarımları, model method'ları | ~250 |
| 5 | [5-deployment.md](.claude/docs/5-deployment.md) | 15 adımlık execution protocol, Docker config, kritik kurallar | ~200 |

---

## ⚡ Özet Akış (15 Adım)

```
ADIM  1: Proje İskeleti          → Klasör + dosya yapısı
ADIM  2: Core MVC Framework      → Router, Controller, Model, View, Session, Validator
ADIM  3: Veritabanı Kurulumu     → schema.sql + seed.sql (81 il, 8 kategori, test data)
ADIM  4: Model Katmanı           → 10 model, tüm iş mantığı method'ları
ADIM  5: Layout & Statik Sayfalar → CSS, Header, Footer, Ana Sayfa, Statik sayfalar
ADIM  6: Auth Sistemi            → Kayıt, Giriş, Çıkış, Şifre sıfırlama, Email doğrulama
ADIM  7: İlan Sistemi            → CRUD, multi-step form, görsel yükleme, galeri
ADIM  8: Arama & Filtreleme      → FULLTEXT arama, dinamik filtreler, cascading dropdown
ADIM  9: Mesajlaşma Sistemi      → İlan bazlı mesajlaşma, AJAX, okundu takibi
ADIM 10: Favori & Profil         → Favori toggle, profil CRUD, avatar yükleme
ADIM 11: Admin Paneli            → Dashboard, kullanıcı/ilan/kategori yönetimi
ADIM 12: Güvenlik Sertleşme      → CSRF, XSS, SQLi, Upload güvenliği, Rate limiting
ADIM 13: SEO Optimizasyonu       → Meta tags, Schema.org, sitemap, canonical URL
ADIM 14: Performans              → Cache, lazy loading, N+1 çözümü, minify
ADIM 15: Docker & Deployment     → Dockerfile, docker-compose, README
```

---

## 🔴 Kritik Kurallar

1. **Her adımdan sonra TEST ET** – Terminal çıktısı kanıt olmadan ilerle yasak
2. **PDO Prepared Statements** – Tüm SQL sorgularında, istisna YOK
3. **`e()` ile XSS koruması** – Tüm kullanıcı çıktılarında
4. **CSRF token** – Tüm POST formlarında
5. **Responsive 320px–1920px** + Dark/Light mode tüm komponentlerde
6. **PHP 8.2 syntax** + PHPDoc yorum satırları zorunlu
