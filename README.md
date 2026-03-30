# 📷 Photobooth

Tarayıcı tabanlı retro photobooth uygulaması. Fotoğraf çek, çerçeve seç, grid oluştur, paylaş.

🌐 **Canlı site:** https://batudemir14.github.io/photobooth/

---

## Özellikler

### Fotoğraf Çekme
- Tarayıcıdan kamera erişimi (Safari ve Chrome destekli)
- Geri sayım: 1, 2, 3, 5, 10 saniye
- Otomatik oturum — seçilen sayıda fotoğrafı arka arkaya çeker
- Flaş efekti her çekimde
- Film şeridinde anlık önizleme
- Tek tek fotoğraf silebilme

### Grid Formatları
| Format | Açıklama |
|--------|----------|
| 2×2 | 4 fotoğraf, kare düzen |
| 1×4 | 4 fotoğraf, dikey şerit |
| 2×1 | 2 fotoğraf, yatay |
| 1×2 | 2 fotoğraf, dikey |
| 1×3 | 3 fotoğraf, dikey şerit |
| 3×1 | 3 fotoğraf, yatay şerit |

### Çerçeve Stilleri
| Çerçeve | Açıklama |
|---------|----------|
| 🎞 Klasik | Krem/kahve, vintage film estetiği, gold kenarlıklar |
| ⬜ Minimal | Beyaz, sade ve temiz |
| 🎂 Doğum Günü | Mor gradient, konfeti, 🎉🎈🎊 emojiler |
| ❤️ Aşk | Kırmızı gradient, 🌹💋💕 emojiler, çift çerçeve |
| 🌸 Bahar | Koyu yeşil, 🌺🌷🦋 çiçek emojiler |
| 🌌 Galaksi | Uzay gradient, yıldızlar, neon mor glow efekti |

### Export & Paylaşım
- Yüksek kalite JPG (hücre başına 600×450 px, fotoğraf 1200×900 px)
- Siyah kenar yok — cover-crop ile tam doluyor
- Tarih damgası her çerçevede
- **İndir** — direkt JPG olarak kaydet
- **Paylaş** — sistem paylaşım menüsü (AirDrop, Mail vb.)
- **Galeriye Kaydet** — iOS'ta fotoğraf galerisine kaydet
- Önizleme penceresi

---

## Kullanım

1. **Kamerayı Aç** → tarayıcı izin ister, izin ver
2. Geri sayım ve fotoğraf sayısını seç
3. **Oturumu Başlat** → poz ver, geri sayım başlar
4. Çekim bittikten sonra grid formatı ve çerçeve seç
5. **İndir / Paylaş / Galeriye Kaydet**

---

## Teknik Detaylar

Saf HTML / CSS / JavaScript — kütüphane yok, framework yok, tek dosya.

- `getUserMedia` API ile yüksek çözünürlüklü kamera erişimi
- `Canvas` API ile fotoğraf çekme, cover-crop ve export
- `Web Share API` ile paylaşım ve galeriye kaydetme
- Her çerçeve stili canvas'ta ayrı render fonksiyonu ile çiziliyor
- GitHub Pages üzerinde barındırılıyor, HTTPS otomatik

---

## Güncelleme
```bash
cat > ~/photobooth/index.html
# kodu yapıştır → Enter → Ctrl+D

cd ~/photobooth && git add index.html && git commit -m "guncelleme" && git push
```

---

## Sürüm Geçmişi

- **v3** — 6 tematik çerçeve (Doğum Günü, Aşk, Bahar, Galaksi), koyu tema, profesyonel tasarım, paylaş & galeriye kaydet
- **v2** — Yüksek kalite çekim (1200×900), cover-crop, 1-2 sn geri sayım eklendi
- **v1** — İlk sürüm: kamera, grid formatları, JPG export
