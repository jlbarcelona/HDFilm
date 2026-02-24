<div align="center">
  
  # 🍿 HDFilm - Premium Sinema Platformu Arayüzü
  **Modern, Hızlı ve Özelleştirilebilir Film Vitrini**

  [![Canlı Önizleme](https://img.shields.io/badge/🔴_Canlı_Önizleme_İçin_Tıklayın-E50914?style=for-the-badge&logo=netflix&logoColor=white)](https://proje1-dizi.blogspot.com/)

  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](#)
  [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](#)
  [![ES6 JavaScript](https://img.shields.io/badge/ES6_Vanilla_JS-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](#)
  [![CodEX Town](https://img.shields.io/badge/Geliştirici-CodEX_Town-00a8ff?style=flat-square)](#)

  *Kullanıcı deneyimini merkeze alan, SEO dostu ve tamamen esnek bir film/dizi platformu önizleme projesi.*

</div>

---

## 📸 Ekran Görüntüleri


| Ana Sayfa (Grid Yapısı) | Film Detay Sayfası | Mobil Görünüm |
| :---: | :---: | :---: |
| ![Ana Sayfa](https://iili.io/qKeTBYN.png) | ![Detay](https://iili.io/qKeAihX.png) | ![Mobil](https://iili.io/qKe7hp2.png) |

---

## ✨ Öne Çıkan Gelişmiş Özellikler

### 🎨 UI/UX Tasarım Mimarisi
* **Kusursuz Grid & Flexbox Mimarisi:** Film afişlerini cihazın ekran genişliğine göre otomatik ölçekleyen (Responsive) akıllı ızgara sistemi.
* **Sinematik Hover Efektleri:** Afişlerin üzerine gelindiğinde pürüzsüz bir "Glassmorphism" efektiyle beliren özet bilgiler, IMDB puanları ve oynat butonları.
* **Dinamik Kategori Filtreleme:** Sayfayı yenilemeden çalışan, kullanıcıların aksiyon, komedi, bilim kurgu gibi türler arasında anında geçiş yapabildiği akıllı menü.
* **Yerleşik Dark Mode Altyapısı:** CSS Variables (Değişkenler) kullanılarak tasarlanmış, tek tıkla gece/gündüz moduna geçebilen renk paleti.

### ⚡ Performans ve Entegrasyon
* **Hızlı Yüklenme (Lazy Loading):** Yüksek çözünürlüklü film afişlerinin sadece ekrana girdiklerinde yüklenmesini sağlayan tarayıcı tabanlı tembel yükleme stratejisi.
* **CodEX Player Tam Uyumluluk:** Film detay sayfalarında, sıfır gecikme ve HLS desteği sunan kardeş projemiz `CodEX Player` ile %100 entegre çalışma yeteneği.
* **Blogger & CMS Uyumlu:** Karmaşık framework'ler içermeyen saf (vanilla) yapısı sayesinde Blogger tema XML'lerine veya WordPress gibi sistemlere kolayca giydirilebilir.

---

## 💻 Çekirdek Kod Mimarisi

HDFilm, temiz kod standartlarına (Clean Code) uygun olarak geliştirilmiştir. İşte arka planda çalışan mimariden bazı örnekler:

### 1. Dinamik Filtreleme Mantığı (`app.js`)
Kullanıcıların filmleri türlerine göre saniyeler içinde filtrelemesini sağlayan, `data-category` niteliklerini kullanan hafif JS motoru.

```javascript
const filterButtons = document.querySelectorAll('.filter-btn');
const movieCards = document.querySelectorAll('.movie-card');

filterButtons.forEach(button => {
    button.addEventListener('click', () => {
        // Aktif buton stilini güncelle
        document.querySelector('.filter-btn.active').classList.remove('active');
        button.classList.add('active');

        const filterValue = button.getAttribute('data-filter');

        movieCards.forEach(card => {
            if (filterValue === 'all' || card.getAttribute('data-category').includes(filterValue)) {
                card.style.display = 'block'; // veya animasyonlu bir class eklenebilir
                setTimeout(() => card.style.opacity = '1', 50);
            } else {
                card.style.opacity = '0';
                setTimeout(() => card.style.display = 'none', 300);
            }
        });
    });
});
```

<div align="center">
<p><b>CodEX Town</b> tarafından yaratıcılık ve tutkuyla kodlanmıştır.</p>
</div>
