- BEM notationları kullanarak bu projeyi tamamlayacağız.
Block > element > modifer methodolojisi. Class isimlerindeki kargaşaya son vermek için kullanıyoruz. Örnek:

.card (blok)
.card__image (element)
.card__button--success (modifier)


https://aaron-clarusway.github.io/google-landing--page/


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

<!-- ----- Header ----- -->

1. satırda öncelikle margin ve padding'i sıfırlıyoruz. box-sizing'i border-box olarak ayarlıyoruz. browserdan kaynaklanabilecek gereksiz boşlukları engellemek için bu yönteme başvuruyoruz. Genel olarak font-size birbirine yakın olduğu için 13px olarak verdik ve font-family olarak arial'ı seçtik. <a> taglerinin altında çizgi olmasını istemiyoruz. sayfanın genelinde olmadığı için <!-- text-decoration: none; --> ekledik.

9. satırda body'ye width olarak 100% verdik ki sayfamızın tamamını kaplasın. 1. satırdaki * ikonuna da verebilirdik.

12. satırda .header'a still vermeye başlıyoruz.
15. ve 17. satırda header iki bölümden oluşuyordu. FLOAT ile .header__left'i sola .header__right'ı da sağa yaslıyoruz.

<ul> tagleri içerisindeki noktaları kaldırmak için <!-- list-style-type: none;  --> kullandık
<ul li> içinde <!-- display: inline-block; --> kullandık. böylece listeler altalta durmayacak ve istediğimiz gibi yanyana şekilde sıralanacak.

28. satırdayız şekil olarak google resmi şu an <ul> taglerinin arasında kalıyor. bunun önüne geçmek için header'ın altına boş bir <div> açıyoruz. buradaki amaç resmi aşağıya alabilmek. daha sonra CSS tarafında bu boş <div> (class="clear") için display: cleariyoruz.

30. satırda header içerisindeki linklerimizi stilize etmeye devam ediyoruz. paddingini, opacity ve hover durumunda verdiği özellikleri girdik.

39. satırda ise sağ tarafı düzenlemeye yavaş yavaş başlıyoruz. öncelikle appicon'u dikey olarak ortaladık. hover durumundaki tepkisini belirledik.

47. satırda sign in butonunu ve hover durumunu düzenledik. böylece header ile işimiz bitti.

<!-- ----- Main ----- -->

62. satırda logoyu düzenliyoruz. verilen height, width ve margini girdik. display'e block vermemizin sebebi ortada tutabilmek. yerini ve konumunu ayarladık.
