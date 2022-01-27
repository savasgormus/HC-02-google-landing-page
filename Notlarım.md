- BEM notationları kullanarak bu projeyi tamamlayacağız.
Block > element > modifer methodolojisi. Class isimlerindeki kargaşaya son vermek için kullanıyoruz. Örnek:

.card (blok)
.card__image (element)
.card__button--success (modifier)


----------------------

HTML 
<link rel="shortcut icon" href="./images/gfavicon.png" type="image/x-icon"> ile faviconu ekledik.

web sayfasını 3 bölümden oluşturacağız. 
Header
Main
Footer

----- Header ----
header'ı oluşturduktan sonra 2 farklı bölüm açıyoruz. böylece header__left ve header__right için <ul> tagi içerisinde listeler oluşturacağız. 
<ul class="header__left">
<ul class="header__right">
About, store, gmail, görseller vs sekmeleri için. bu sekmeler link olduğu için

<li><a href=""></a></li> ile bu linkleri oluşturduk.
kısayolu: li*4>a   => 4 tane liste elemanı ve içerisinde a(link olacak)

daha sonra stil vereceğimiz için class isimleri verdik:
class="header__right--appicon"
class="header__right--button"

----- Main ----