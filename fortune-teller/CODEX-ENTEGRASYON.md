# ED Labs — Fortune Teller (Codex Entegrasyonu)

## Kaynak
Bu klasördeki `index.html` dosyası, ED Labs'e taşınacak bağımsız tarot uygulamasının eksiksiz HTML/CSS/JavaScript kodudur. Render'a ihtiyaç duymaz. 78 Rider–Waite–Smith kartının kimlikleri ve adları dosyanın içindedir.

## Codex'e görev
ED Labs projesini aç, mevcut yapıyı incele ve `fortune-teller/index.html` dosyasını projeye dahil et. Ana sayfaya **Fortune Teller** deneyim kartı ekle, deneyimi `/fortune-teller/` yolunda aç. Diğer ED Labs oyunlarını, rotalarını ve tasarımını değiştirme. Render'da yayınlama; ED Labs'in kendi mevcut yayın akışını kullan.

React/Vite projesinde gerekirse `public/fortune-teller/index.html` olarak kopyala. HTML'yi React JSX içine ham olarak yapıştırma. Proje farklı bir base path kullanıyorsa uygun URL ile eşleştir.

## Özellikler
- 78 benzersiz tarot kartı, Fisher–Yates ile karıştırılan kapalı deste
- Yatay parmak takibi + 3D perspektifli fiziksel deste/çark + momentum + yaylı snap
- Telefonun büyük bölümünü kaplayan kartlar
- Yukarı sürükleyerek kart seçme; seçim sayısı serbest
- Shuffle, Kartları Aç, Yeni Açılım ve yatay sonuç kaydırma
- Gerçek Rider–Waite–Smith kart görselleri; yedek CDN bağlantıları

## Önemli: görsel dosyaları
`index.html` şu an kart görsellerini CDN'den yükler. ED Labs'i harici CDN'den bağımsızlaştırmak için gerçek 78 JPG dosyasını `https://github.com/sixseeds/tarot-api/tree/main/cards` kaynağından `public/fortune-teller/cards/` dizinine al, görsel URL'sini yerel yola değiştir. Dosya isimleri `ar00.jpg`…`ar21.jpg`, `wa01.jpg`…`wa14.jpg`, `cu01.jpg`…`cu14.jpg`, `sw01.jpg`…`sw14.jpg`, `pe01.jpg`…`pe14.jpg` şeklindedir.

## Testler
1. Toplam 78 kart ve tekrar etmeyen karışık sıralama.
2. Yatay sürüklemede kesintisiz hareket, hızlı atışta momentum ve yumuşak snap.
3. Yukarı sürükleyerek seçilen kartın desteden çıkması.
4. İstenilen sayıda kartla açılım; gerçek kart ön yüzünün doğru görünmesi.
5. Shuffle ve Yeni Açılım'ın sorunsuz çalışması.
6. ED Labs'in diğer sayfalarının etkilenmemesi.

Tarot çizimleri: Pamela Colman Smith, Rider–Waite–Smith 1909. Kullanım koşullarını dağıtım öncesi doğrula.
