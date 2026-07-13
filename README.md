# Memorya Dekor

> MDF & ahşap duvar ve masa dekorasyon sipariş platformu.

Lazer kesim, UV baskı ve plexi ürünleri kapsayan, uçtan uca geliştirilmiş bir e-ticaret platformu. Güvenli ödeme altyapısı, fotoğraf yönetimi ve tam kapsamlı admin paneli ile donatılmış.

🌐 **Canlı:** [memoryadekor.com](https://memoryadekor.com)

---

## 🚀 Özellikler

- **Ürün Kataloğu** — Lazer kesim, UV baskı ve plexi kategorilerinde çok sayıda ürün. Her ürün için galeri, varyant seçimi ve detay sayfası.
- **Güvenli Ödeme Akışı** — iyzico entegrasyonu ile 3D Secure destekli ödeme. Sipariş oluşturma → ödeme başlatma → callback doğrulama zinciri backend üzerinden yönetiliyor. Duplicate callback ve başarısız ödemeler otomatik temizleniyor.
- **Fotoğraf Yönetimi** — Ürün görselleri private Supabase Storage'a kaydediliyor. Signed URL sistemi ile güvenli erişim.
- **Admin Paneli** — Sipariş takibi, aşama yönetimi, kargo girişi ve otomatik kargo bildirimi. Finans dashboard'u ile aylık gelir/gider analizi ve ürün bazlı kar marjı hesaplama.
- **Otomatik E-posta Bildirimleri** — Resend API ile sipariş onayı, ödeme doğrulama ve kargo bildirimi mailleri otomatik gönderiliyor.
- **SEO** — Her ürün sayfasına özel meta tag, Open Graph, Twitter Card ve JSON-LD structured data. Google Search Console ve sitemap entegrasyonu.

---

## 🛠 Tech Stack

### Frontend
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

### Backend & Altyapı
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-1C1C1C?style=for-the-badge&logo=supabase&logoColor=3ECF8E)

**Üçüncü Parti:** iyzico (Ödeme), Resend (E-posta), Vercel (Hosting)

---

## 📐 Sistem Mimarisi

```
[ İstemci (React + Vite) ]
          │  HTTPS / REST
          ▼
[ Express.js API ]
          │
          ├──► [ PostgreSQL & Storage (Supabase) ]
          │         └── Siparişler, ürünler, ürün görselleri
          │
          ├──► [ iyzico Payment Gateway ]
          │         └── 3D Secure, callback doğrulama
          │
          └──► [ Resend API ]
                    └── Sipariş, ödeme, kargo mailleri
```

---

## 📸 Ekran Görüntüleri

> Siteyi ziyaret edebilirsiniz → [memoryadekor.com](https://memoryadekor.com)

---

## Durum

✅ Aktif olarak yayında — gerçek kullanıcı siparişleri alınıyor
