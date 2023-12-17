# Game_Portal
**Özel Owl Carousel ve Menü Açma/Kapatma İşlevi**

Bu jQuery ve SASS (CSS derleme dili) kullanılarak oluşturulmuş kod parçaları, özel bir Owl Carousel ve bir menüyü açma/kapatma işlevini içerir. Aşağıda, bu kodları kullanarak yapılan işlevselliği ve özellikleri açıklayan sade ve anlaşılır bir açıklama yer almaktadır:

**JavaScript ve jQuery Kodu:**

Bu kod, belirli bir Owl Carousel'ı özelleştirir ve menü açma/kapatma işlevselliğini ekler.

```javascript
$(document).ready(function(){
    // Owl Carousel Özelleştirmesi
    let owl = $(".owl-carousel").owlCarousel({
        autoplay: false,
        dots: true,
        dotsData: true,
        loop: true,
        nav: false,
        items: 1
    });

    // Owl Carousel'daki noktalara tıklandığında ilgili slayda geçiş
    $('.owl-dot').click(function() {
        owl.trigger('to.owl.carousel', [$(this).index(), 1000]);
    });
});

// Menü Açma/Kapatma İşlevi
$('#chek').change(function() {
    if($(this).is(":checked")) {
        $('.nav-header').addClass('active');
    } else {
        $('.nav-header').removeClass('active');
    }
});
```

**Açıklama:**

- **Owl Carousel Özelleştirmesi:**
  - Carousel ayarları yapılandırılır (`autoplay`, `dots`, `loop`, vb.).
  - Owl Carousel, belirli bir noktaya geçiş yapmak için noktalara tıklanabilmesi için `$('.owl-dot').click` olayı dinlenir.

- **Menü Açma/Kapatma İşlevi:**
  - `#chek` öğesinin (muhtemelen bir checkbox veya toggle düğmesi) durum değişikliği dinlenir.
  - Checkbox seçiliyse, `.nav-header` öğesine "active" sınıfı eklenir ve menü görünür hale gelir.
  - Checkbox seçili değilse, "active" sınıfı kaldırılır ve menü gizlenir.

**Kullanılan Teknolojiler:**
- jQuery: Sayfa etkileşimleri ve DOM manipülasyonu için.
- Owl Carousel: Özel bir Carousel (kaydırıcı) oluşturmak için.
- SASS: CSS kodlarını daha düzenli ve modüler hale getirmek için kullanılır.

Bu kodlar, belirtilen Carousel'ı özelleştirmek ve bir menüyü açma/kapatma işlevselliği eklemek amacıyla kullanılır. Projenin gereksinimlerine göre özelleştirilebilir ve genişletilebilir.
