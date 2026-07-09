# veloralpcase

# 🎃 Halloween Archery: Gothic Combo Edition

Cadılar Bayramı temalı, fizik tabanlı ve yüksek tempolu bir arcade okçuluk oyunu. Tamamen harici kütüphanesiz (Pure JS & Canvas HTML5) geliştirilen bu projede, tekinsiz bir gecede uçuşan canavarları avlayarak en yüksek skoru elde etmeye çalışın!

---

## 🕹️ Nasıl Oynanır?

Oyun tamamen dokunmatik ekranlar ve fare kontrolleri için optimize edilmiştir:

*   **Serbest Nişan Alma ve Fırlatma:** Ekranın **herhangi bir noktasından** parmağınızı veya farenizi sol tıkla basılı tutup geriye doğru çekin. Çektiğiniz mesafe yayın gücünü, açısı ise yönünü belirler.
*   **Akıllı Tahmin Çizgisi:** Yayı çekerken ekranda beliren kesik yeşil noktalar, okun yerçekimine göre izleyeceği **gerçek fiziksel yörüngeyi** gösterir.
*   **Yay Hakkı (Can) Mekaniği:** Oyuna 3 yay hakkı ile başlarsınız. Attığınız ok herhangi bir canavarı vurursa **hakkınız eksilmez**. Ancak ok hiçbir şeye çarpmadan ekran dışına çıkarsa 1 yay hakkınız gider.
*   **💥 Zincirleme Reaksiyon (Combo Sistem):** Bir canavarı vurduğunuzda, canavar doğrudan ölmez; okun ivmesiyle **takla atarak yere doğru düşmeye başlar**. Eğer düşen canavar havada süzülen başka bir canavara çarparsa onu da düşürür! 
    *   Her zincirleme vuruş size **+1 Yay Hakkı** kazandırır ve puanınızı katlar (`COMBO 2X`, `3X`...).
*   **Duraklatma (Pause):** Sağ üstteki SVG ikonuna tıklayarak oyunu istediğiniz an dondurabilir, ekrana tekrar dokunarak kaldığınız yerden devam edebilirsiniz.
*   **Oyun Bitişi (Game Over):** Yay hakkınız `0` olduğunda oyun biter. Skorunuz en yüksek skoru geçtiyse tarayıcı hafızasına (`localStorage`) kaydedilir. Yeniden başlamak için ekrana dokunmanız yeterlidir.

---

## 🚀 İlham Alınan Oyunlar ve Konsept Farkı

### İlham Kaynakları:
*   **Angry Birds:** Fizik tabanlı çek-bırak (slingshot) nişan alma mekaniği ve yerçekimli yörünge tahmin mantığı doğrudan bu klasikten ilham almıştır.
*   **F.E.A.R. / Resident Evil (Atmosfer):** Oyundaki seslerin minimalist, sakin ama tekinsiz yapısı ile Game Over ekranındaki gotik parlamalar klasik korku oyunlarının arayüz estetiğinden esinlenmiştir.

### Konseptin Farkı ve Benzersiz Yönleri:
1.  **Ragdoll Canavar Kombosu:** Sıradan okçuluk oyunlarında vurulan düşman yok olur. Bu oyunda ise vurulan düşman bir kütleye dönüşerek diğer düşmanları avlamanızı sağlayan bir silaha (zincirleme reaksiyona) dönüşür.
2.  **Sıfır Link Bağımlılığı (Hardware Audio API):** Oyun hiçbir harici `.mp3` veya `.wav` ses dosyasına ihtiyaç duymaz. Tarayıcının donanımsal ses kartını (`Web Audio API`) bir sentezleyici (synthesizer) gibi kullanarak tüm atış ve tiz darbe seslerini kodla gerçek zamanlı üretir. Bağlantı kopma veya ses yüklenmeme derdi yoktur.
3.  **Mobil Odaklı UI Temizliği:** Tarayıcıların mobil cihazlarda butonlara tıklarken çıkardığı klasik sinir bozucu mavi gölgeler (`tap-highlight`) ve çerçeveler CSS seviyesinde tamamen temizlenmiş, pürüzsüz bir arcade deneyimi sağlanmıştır.

---

## ⚠️ Bilinen Eksiklikler & Geliştirme Önerileri

Oyun şu an kararlı ve pürüzsüz çalışmaktadır, ancak projenin ilerleyen aşamalarında eklenebilecek bilinen eksiklikler ve açık noktalar şunlardır:

*   **Varyasyon Eksikliği:** Canavarlar şu an sadece farklı görsellere sahip. Gelecek güncellemelerde daha hızlı giden "Yarasalar" veya vurulması daha zor olan zırhlı canavarlar eklenebilir.
*   **Zorluk Derecesi (Scaling):** Skor arttıkça canavarların geliş hızı sabit kalmaktadır. Oyun süresine bağlı olarak hızlanan bir zorluk eğrisi (progression sistemi) eklenebilir.
*   **Müzik Altyapısı:** Donanımsal ses sistemi efektlerde harika çalışsa da arkada sürekli çalacak melodik bir korku müziği sentezlemek yerine harici bir sinematik soundtrack loop'u entegre edilebilir.