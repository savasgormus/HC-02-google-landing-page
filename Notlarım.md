- BEM notationları kullanarak bu projeyi tamamlayacağız.
Block > element > modifer methodolojisi. Class isimlerindeki kargaşaya son vermek için kullanıyoruz. Örnek:

.card (blok)
.card__image (element)
.card__button--success (modifier)

<!-- --------------------- HTML -------------------------  -->
<link rel="shortcut icon" href="./images/gfavicon.png" type="image/x-icon"> ile faviconu ekledik.

web sayfasını 3 bölümden oluşturacağız. 
Header
Main
Footer

<!-- ----- Header ---- -->
header'ı oluşturduktan sonra 2 farklı bölüm açıyoruz. böylece header__left ve header__right için <ul> tagi içerisinde listeler oluşturacağız. 
<ul class="header__left">
<ul class="header__right">
About, store, gmail, görseller vs sekmeleri için. bu sekmeler link olduğu için

<li><a href=""></a></li> ile bu linkleri oluşturduk.
kısayolu: li*4>a   => 4 tane liste elemanı ve içerisinde a(link olacak)

daha sonra stil vereceğimiz için class isimleri verdik:
class="header__right--appicon"
class="header__right--button"

<!-- ----- Main ----- -->
google logosunu img olarak yükledik.(html 29.satır)
daha sonra logonun altına denk gelecek arama çubuğunu oluşturacağız. fakat burayı bir div içerisine alıp oluşturmak daha mantıklı çünkü birden fazla öğeye still vermemiz gerekecek.
31, 32 ve 32. satırda arama çubuğu olarak kullanılacak alanın öğelerini ekliyoruz. Image, Input alanı ve de link içerisinde bir mikrofon simgesi.

36. satırda yeni bir div açıyoruz. arama çubuğunun altında bulunan butonları stilize etmek için.

37. satırdan itibaren 2 tane button oluşturuyoruz. class isimlerini left ve right şeklinde ayrı verdik çünkü stillendirmede bize kolaylık sağlayacak.
<button class="main__--left"></button>
<button class="main__--right"></button>

41. <p class="main__language">Other Languages you can use Google: <a href="#">English</a></p>
satırda tekrar bi div açtık ve dil seçenekleri ile ilgili <p> tagini oluşturduk. burada div açmak opsiyonel fakat işimizi kolaylaştırır.

<!-- ----- Footer ----- -->
footer 2 bölümden oluştuğu için 2 farklı <div> oluşturacağız.
fakat footer__bottom yine header'daki gibi 2 farklı alandan oluşuyor. yani yine <ul> taglerini kullanarak footer__bottom--left ve footer__bottom--right olarak class ismi vereceğiz. hepsi link olduğu için şu şekilde yapıyoruz.

<div class="footer__bottom">
            <ul class="footer__bottom--left">
                <li><a href=""></a></li>
aynı şekilde footer__bottom--right için de ul oluşturduk ver HTML kısmını bitirdik.

<!-- ----------------------------------------- CSS --------------------------------------------- -->