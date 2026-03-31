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
| Klasik | Krem kagit dokusu, altin kose susleri, vintage estetik |
| Minimal | Beyaz mat, golge efektli hucre kenarliklari, modern tipografi |
| Dogum Gunu | Mor gradient, renkli konfeti sekilleri (daire, serit, ucgen, yildiz), isiltili dekor |
| Ask | Kirmizi gradient, bezier kalp desenleri, vignette efekti |
| Bahar | Yesil gradient, yaprak/botanik dekorasyonlar, isik lekeleri |
| Galaksi | Uzay gradient, nebula renk izleri, cok katmanli yildiz alani, difraksiyon efektleri |

### Ek Ozellikler
- **Duzenle modu** — fotografa tikla veya Duzenle butonuna bas, tam ekran overlay'da cerceve degistir, fotograf sirasini degistir (tap-to-swap), canli onizleme
- **Ayna modu** — acma/kapama butonu
- **Tam ekran modu** — viewfinder'i fullscreen yapma
- **Poz onerileri** — Her fotograf oncesi ekranda gosteriliyor, Komik/Romantik/Klasik kategoriler
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

---

## Kullanim

1. **Kamerayi Ac** — tarayici izin ister, izin ver
2. Geri sayim ve fotograf sayisini sec
3. Istersen filtre, cerceve ve grid formatini ayarla
4. **Oturumu Baslat** — poz ver, geri sayim baslar
5. Cekim bittikten sonra **Duzenle** ile cerceve/siralama degistir veya direkt indir
6. **Indir / GIF Olustur / Paylas / Galeriye Kaydet**

---

## Mobil Deneyim

Uygulama mobil oncelikli tasarlandi:
- Dikey 3:4 viewfinder (selfie dostu)
- Yatay kaydirmali film seridi
- Fotograf siralama ok butonlari (mobilde kolay kullanim)
- Fotografa tiklayinca duzenle modu aciliyor
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
- Pixel bazli manuel filtre uygulama (Safari/iOS uyumlu, ctx.filter bagimli degil)
- Her cerceve stili canvas'ta ayri render fonksiyonu ile ciziliyor
- GitHub Pages uzerinde barindiriliyor, HTTPS otomatik

---

## Surum Gecmisi

- **v6.1** — Her fotograf oncesi poz onerisi, checkbox tik stili, mobil ok butonlariyla siralama, fotografa tikla duzenle, layout yeniden duzenleme
- **v6** — Bug fixler (mobil baslik hizalama, filtre export Safari uyumu, metin overlay cakismasi), duzenle modu, cerceve render iyilestirmeleri (doku, golge, dekorasyon), UI polish (header shimmer, panel glow, kayit border efekti)
- **v5** — Mobil oncelikli responsive tasarim, toast bildirimleri, konfeti, countdown progress bar & beep, tam ekran, kamera degistirme, lightbox, klavye kisayollari
- **v4** — Filtreler, deklansor sesi, ayna modu, surukle-siralama, metin yerlestirme, Instagram formati, GIF export, poz onerileri, Turkce duzeltmeleri, UI iyilestirmeleri
- **v3** — 6 tematik cerceve, koyu tema, profesyonel tasarim, paylas & galeriye kaydet
- **v2** — Yuksek kalite cekim (1200x900), cover-crop, 1-2 sn geri sayim eklendi
- **v1** — Ilk surum: kamera, grid formatlari, JPG export
