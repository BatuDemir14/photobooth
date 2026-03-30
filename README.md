# Photobooth

Tarayici tabanli, mobil oncelikli retro photobooth uygulamasi. Fotograf cek, filtre uygula, cerceve sec, grid olustur, paylas.

**Canli site:** https://batudemir14.github.io/photobooth/

---

## Ozellikler

### Fotograf Cekme
- Tarayicidan kamera erisimi (Safari ve Chrome destekli)
- On/arka kamera degistirme (coklu kamerali cihazlarda)
- Geri sayim: 1, 2, 3, 5, 10 saniye
- Gorsel countdown progress bar
- Countdown beep sesi (Web Audio API)
- Otomatik oturum — secilen sayida fotografi arka arkaya ceker
- Flas efekti + deklansor sesi her cekimde
- Film seridinde anlik onizleme
- Tek tek fotograf silebilme
- Surukleme ile fotograf siralama

### Filtreler (Canli Onizleme)
| Filtre | Aciklama |
|--------|----------|
| Normal | Filtre yok |
| Siyah-Beyaz | Grayscale |
| Sepya | Sicak vintage ton |
| Soluk | Dusuk kontrast, pastel |
| Canli | Yuksek doygunluk |

### Grid Formatlari
| Format | Aciklama |
|--------|----------|
| 1x1 | Tek fotograf, kare (Instagram) |
| 2x1 | 2 fotograf, yatay |
| 1x2 | 2 fotograf, dikey |
| 2x2 | 4 fotograf, kare duzen |
| 2x2 Kare | 4 fotograf, kare export |
| 1x3 | 3 fotograf, dikey serit |
| 3x1 | 3 fotograf, yatay serit |
| 1x4 | 4 fotograf, dikey serit |

### Cerceve Stilleri
| Cerceve | Aciklama |
|---------|----------|
| Klasik | Krem/kahve, vintage film estetigi, gold kenarliklar |
| Minimal | Beyaz, sade ve temiz |
| Dogum Gunu | Mor gradient, konfeti, emoji dekorasyonlar |
| Ask | Kirmizi gradient, kalp ve gul emojiler, cift cerceve |
| Bahar | Koyu yesil, cicek emojiler |
| Galaksi | Uzay gradient, yildizlar, neon mor glow efekti |

### Ek Ozellikler
- **Ayna modu** — acma/kapama butonu
- **Tam ekran modu** — viewfinder'i fullscreen yapma
- **Poz onerileri** — Komik, Romantik, Klasik kategorilerde rastgele pozlar
- **Metin yerlestirme** — Isim ve tarih overlay'i export uzerinde
- **Konfeti animasyonu** — cekim tamamlaninca kutlama efekti
- **Toast bildirimleri** — sik bildirim sistemi (alert yok)
- **Fotograf lightbox** — thumbnail'a tikla, buyuk onizle, oklarla gezin
- **Klavye kisayollari** — Space (baslat), R (sifirla), M (ayna), F (tam ekran)

### Export & Paylasim
- Yuksek kalite JPG (hucre basina 600x450 px, fotograf 1200x900 px)
- Cover-crop ile tam doluyor
- Tarih damgasi her cercevede
- **Indir** — direkt JPG olarak kaydet
- **GIF Olustur** — fotograflari animasyonlu GIF olarak indir
- **Paylas** — sistem paylasim menusu (AirDrop, Mail vb.)
- **Galeriye Kaydet** — iOS'ta fotograf galerisine kaydet
- Onizleme penceresi

---

## Kullanim

1. **Kamerayi Ac** — tarayici izin ister, izin ver
2. Geri sayim ve fotograf sayisini sec
3. Istersen filtre, cerceve ve grid formatini ayarla
4. **Oturumu Baslat** — poz ver, geri sayim baslar
5. Cekim bittikten sonra ayarlari degistir veya direkt indir
6. **Indir / GIF Olustur / Paylas / Galeriye Kaydet**

---

## Mobil Deneyim

Uygulama mobil oncelikli tasarlandi:
- Dikey 3:4 viewfinder (selfie dostu)
- Yatay kaydirmali film seridi
- Buyuk dokunma alanlari (min 44px)
- Safe area destegi (centikli telefonlar)
- On/arka kamera gecisi
- Tam ekran modu
- Reduce motion medya sorgusu destegi

---

## Teknik Detaylar

Saf HTML / CSS / JavaScript — kutuphane yok, framework yok, tek dosya.

- `getUserMedia` API ile yuksek cozunurluklu kamera erisimi
- `Canvas` API ile fotograf cekme, cover-crop ve export
- `Web Audio API` ile deklansor sesi ve countdown beep
- `Web Share API` ile paylasim ve galeriye kaydetme
- `Fullscreen API` ile tam ekran modu
- Inline LZW encoder ile GIF olusturma
- CSS filtreleri ile canli video onizleme
- Her cerceve stili canvas'ta ayri render fonksiyonu ile ciziliyor
- GitHub Pages uzerinde barindiriliyor, HTTPS otomatik

---

## Surum Gecmisi

- **v5** — Mobil oncelikli responsive tasarim, toast bildirimleri, konfeti, countdown progress bar & beep, tam ekran, kamera degistirme, lightbox, klavye kisayollari
- **v4** — Filtreler, deklansor sesi, ayna modu, surukle-siralama, metin yerlestirme, Instagram formati, GIF export, poz onerileri, Turkce duzeltmeleri, UI iyilestirmeleri
- **v3** — 6 tematik cerceve, koyu tema, profesyonel tasarim, paylas & galeriye kaydet
- **v2** — Yuksek kalite cekim (1200x900), cover-crop, 1-2 sn geri sayim eklendi
- **v1** — Ilk surum: kamera, grid formatlari, JPG export
