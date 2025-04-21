<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sırtaş Tesbihcilik - Anasayfa</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    html {
      scroll-behavior: smooth;
    }
    .slider {
      display: flex;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      scroll-behavior: smooth;
    }
    .slider::-webkit-scrollbar {
      display: none;
    }
    .slider img {
      scroll-snap-align: start;
      flex-shrink: 0;
      width: 100%;
      height: 400px;
      object-fit: cover;
    }
    .slider-buttons {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 100%;
      display: flex;
      justify-content: space-between;
      padding: 0 1rem;
      z-index: 10;
    }
    .slider-buttons button {
      background-color: rgba(0, 0, 0, 0.5);
      color: white;
      padding: 0.5rem;
      border-radius: 9999px;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body class="bg-gray-900 text-white font-sans">

  <!-- Navbar -->
  <header class="bg-gray-800 text-yellow-400 p-4">
    <div class="flex flex-col space-y-4">
      <div class="flex justify-between items-center w-full">
        <div class="flex items-center space-x-2">
          <h1 class="text-3xl font-bold">Sırtaş Tesbih</h1>
          <img src="WhatsApp Image 2025-04-14 at 23.14.19.jpeg" alt="Sırtaş Logo" class="h-6 opacity-70 mt-1">
        </div>
        <div class="flex-1 flex justify-center">
          <input type="text" placeholder="Ürün ara..." class="rounded p-2 text-black w-64">
        </div>
        <div class="flex items-center space-x-4">
          <a href="giris-yap.html" class="hover:text-yellow-300">Giriş Yap</a>
          <a href="#" class="hover:text-yellow-300">Favorilerim</a>
          <a class="wishlist label-down link d-xs-show" href="/siparislerim"><i class=" w-icon-truck"></i><span class="wishlist-label d-lg-show">Siparişlerim</span></a>
          <a id="cartButton" href="sepet.html" class="hover:text-yellow-300 relative flex items-center hidden">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2 9m5-9v9m4-9v9m4-9l2 9" />
            </svg>
            Sepet
            <span id="cartCount" class="absolute -top-2 -right-3 bg-red-600 text-white rounded-full text-xs px-1.5">0</span>
            <span id="cartTotal" class="ml-2 text-sm text-yellow-400 hidden">₺0</span>
          </a>
        </div>
      </div>

      <!-- Menü Butonu + Navigasyon Yanyana -->
      <div class="flex flex-wrap justify-center items-center gap-6 mt-4">
        <div class="dropdown flex flex-col items-start relative">
          <div class="side-menu-button flex items-center space-x-2 bg-gray-700 text-white px-4 py-2 rounded cursor-pointer" aria-haspopup="true" aria-expanded="false">
            <i class="i-navigation-menu"></i>
            <p class="text-sm font-medium">TÜM KATEGORİLER</p>
            <span class="new-badge bg-red-500 text-white text-xs px-2 py-0.5 rounded-full ml-2">Yeni</span>
          </div>
          <div class="dropdown-menu hidden w-48 bg-gray-800 text-white rounded shadow-lg py-2 mt-2 space-y-1">
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Oltu Taşı</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Kuka</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Ateş Kehribar</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Damla Kesim</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Yuvarlak Kesim</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Özel Tasarım</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Koleksiyonluk</a>
          </div>
        </div>

        <!-- Üst Menü -->
        <nav class="flex space-x-6">
          <a href="#slider" class="hover:text-yellow-300">Anasayfa</a>
          <a href="#hakkimizda" class="hover:text-yellow-300">Hakkımızda</a>
          <a href="#iletisim" class="hover:text-yellow-300">İletişim</a>
        </nav>
      </div>
    </div>
  </header>

  <!-- Vitrin Slider -->
  <section class="my-6 max-w-5xl mx-auto relative" id="slider">
    <div class="slider rounded-lg shadow-lg">
      <img src="images/vitrin1.jpg" alt="Vitrin 1">
      <img src="images/vitrin2.jpg" alt="Vitrin 2">
      <img src="images/vitrin3.jpg" alt="Vitrin 3">
      <img src="images/vitrin4.jpg" alt="Vitrin 4">
      <img src="images/vitrin5.jpg" alt="Vitrin 5">
    </div>
    <div class="slider-buttons">
      <button id="prevBtn">⟨</button>
      <button id="nextBtn">⟩</button>
    </div>
  </section>

  <!-- Hakkımızda Kısmı -->
  <section class="max-w-4xl mx-auto my-12 px-4 text-center" id="hakkimizda">
    <h2 class="text-3xl text-yellow-400 font-bold mb-4">Hakkımızda</h2>
    <p class="text-gray-300 leading-relaxed">
      Sırtaş Tesbihcilik, Erzurum’un Kadim Zanaat Geleneğinden İlham Alarak Kurulan Özel Bir Markadır. Her Bir Tespih Tanesinde, Yılların Birikimi Ve El İşçiliğinin Zarafeti Saklıdır. “Her Tane Bir Sır Gibi” Sloganıyla Çıktığımız Bu Yolda, Hem Klasik Hem De Modern Lazer Kesim Tekniklerini Kullanarak Benzersiz Koleksiyonlar Üretiyoruz.<br><br>
      Amacımız; Tespih Kültürünü Yaşatmak, Her Beğeniye Hitap Eden Tasarımlarla Koleksiyonerlerin Ve Tespih Severlerin Gönlünde Yer Edinmektir. Tüm Ürünlerimiz Özgün, Kaliteli Ve Özel Detaylarla Donatılmıştır. Sırtaş, Sadece Bir Tespih Değil, Geçmişten Geleceğe Uzanan Bir Sanat Yolculuğudur.
    </p>
  </section>

  <!-- Öne Çıkan Ürünler Başlık -->
  <section class="max-w-6xl mx-auto mt-12 px-4">
    <h2 class="text-3xl text-yellow-400 font-bold mb-6 text-center">Öne Çıkan Ürünler</h2>
  </section>

  <!-- Ürün Kartları -->
  <section class="max-w-6xl mx-auto py-8 px-4 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
    <p class="text-gray-400 text-center col-span-full">Yeni ürünler çok yakında eklenecek...</p>
  </section>

  <!-- Müşteri Yorumları Bölümü -->
  <section class="max-w-6xl mx-auto mt-12 px-4" id="yorumlar">
    <h2 class="text-3xl text-yellow-400 font-bold mb-6 text-center">Müşteri Yorumları</h2>
    <div class="flex space-x-4 overflow-x-auto pb-4">
      <div class="bg-gray-800 p-4 rounded-lg min-w-[280px] flex-shrink-0 shadow-md">
        <p class="text-gray-300 mb-2">"Tesbih kalitesi harika, lazer detaylar gerçekten çok etkileyici."</p>
        <div class="text-yellow-400 font-semibold">- Mehmet A.</div>
        <div class="text-yellow-400 mt-1">★★★★★</div>
      </div>
      <div class="bg-gray-800 p-4 rounded-lg min-w-[280px] flex-shrink-0 shadow-md">
        <p class="text-gray-300 mb-2">"Siparişim hızlı geldi ve paketleme çok özenliydi. Teşekkür ederim."</p>
        <div class="text-yellow-400 font-semibold">- Elif K.</div>
        <div class="text-yellow-400 mt-1">★★★★☆</div>
      </div>
      <div class="bg-gray-800 p-4 rounded-lg min-w-[280px] flex-shrink-0 shadow-md">
        <p class="text-gray-300 mb-2">"Böylesine zarif işçilik uzun zamandır görmemiştim."</p>
        <div class="text-yellow-400 font-semibold">- Hüseyin T.</div>
        <div class="text-yellow-400 mt-1">★★★★★</div>
      </div>
    </div>
  </section>

  <!-- Footer + Sosyal Medya -->
  <footer class="bg-gray-800 text-white p-6 mt-10 text-sm" id="iletisim">
    <div class="max-w-6xl mx-auto flex flex-col items-center space-y-3">
      <div> Müşteri Hizmetleri: <strong>0850 326 9325</strong> <span class="text-gray-400 ml-2">(Hafta içi 09:00 - 18:00)</span></div>
      <div class="flex space-x-4 mt-2">
        <a href="https://www.facebook.com" target="_blank" class="text-blue-600 text-2xl"><i class="fab fa-facebook-square"></i></a>
        <a href="https://www.instagram.com" target="_blank" class="text-pink-500 text-2xl"><i class="fab fa-instagram"></i></a>
        <a href="https://wa.me/905555555555" target="_blank" class="text-green-500 text-2xl"><i class="fab fa-whatsapp"></i></a>
        <a href="tel:08503269325" class="text-yellow-400 text-2xl"><i class="fas fa-phone-alt"></i></a>
        <a href="mailto:destek@sirtastesbih.com" class="text-yellow-400 text-2xl"><i class="fas fa-envelope"></i></a>
      </div>
    </div>
  </footer>

  <script>
    // Slider butonları çalıştırma scripti
    const slider = document.querySelector('.slider');
    const nextBtn = document.getElementById('nextBtn');
    const prevBtn = document.getElementById('prevBtn');

    nextBtn.addEventListener('click', () => {
      slider.scrollBy({ left: slider.offsetWidth, behavior: 'smooth' });
    });

    prevBtn.addEventListener('click', () => {
      slider.scrollBy({ left: -slider.offsetWidth, behavior: 'smooth' });
    });
  </script>
</body>
</html>
