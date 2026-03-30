# 📷 Photobooth

Tarayıcı tabanlı, kamera erişimi olan retro photobooth uygulaması. Fotoğraf çek, grid oluştur, JPG olarak indir.

🌐 **Canlı site:** https://batudemir14.github.io/photobooth/

---

## Özellikler

### Fotoğraf Çekme
- Tarayıcıdan kamera erişimi (Safari ve Chrome destekli)
- Geri sayım seçeneği: 1, 2, 3, 5, 10 saniye
- Otomatik oturum: seçilen sayıda fotoğrafı arka arkaya çeker
- Flaş efekti her çekimde
- Film şeridinde anlık önizleme
- Tek tek fotoğraf silebilme

### Grid Formatları
- **2×2** — 4 fotoğraf, kare düzen
- **1×4** — 4 fotoğraf, dikey şerit
- **2×1** — 2 fotoğraf, yatay
- **1×2** — 2 fotoğraf, dikey
- **1×3** — 3 fotoğraf, dikey şerit
- **3×1** — 3 fotoğraf, yatay şerit

### Çerçeve Stilleri
- **Klasik** — Krem/kahve, vintage film estetiği
- **Beyaz** — Minimal, temiz
- **Karanlık** — Siyah, sinematik
- **Neon** — Mor/cyan glow efekti
- **Polaroid** — Beyaz kenarlı klasik format
- **Retro** — Altın/sepia tonları, köşe süsleri

### Export
- Yüksek kalite JPG (fotoğraf başına 1200×900 px, export hücresi 600×450 px)
- Siyah kenar yok — fotoğraflar oranı korunarak tam hücreyi dolduruyor
- Tarih damgası
- Önizleme veya direkt indirme

---

## Kullanım

1. **Kamerayı Aç** butonuna tıkla → tarayıcı izin ister
2. Geri sayım süresini ve fotoğraf sayısını seç
3. **Oturumu Başlat** → geri sayım başlar, poz ver
4. Tüm fotoğraflar çekildikten sonra grid formatı ve çerçeve stili seç
5. **JPG İndir** veya **Önizle**

---

## Teknik

Saf HTML/CSS/JavaScript — hiçbir kütüphane veya framework kullanılmadı. Tek dosya, sunucu gerektirmez.

- `getUserMedia` API ile kamera erişimi
- `Canvas` API ile fotoğraf çekme ve export
- Cover-crop mantığı: video 4:3 oranında kırpılarak siyah kenar oluşmuyor
- GitHub Pages üzerinde barındırılıyor

---

## Güncelleme
```bash
cat > ~/photobooth/index.html
# kodu yapıştır → Enter → Ctrl+D

cd ~/photobooth && git add index.html && git commit -m "guncelleme" && git push
```
