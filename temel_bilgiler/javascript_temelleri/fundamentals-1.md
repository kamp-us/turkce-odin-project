### Giriş
JavaScript'e dalalım!

### Ders Özeti
Bu bölümde öğreneceğiniz konuların genel bir özeti bulunmaktadır.

* Bir değişken nasıl tanımlanır?
* Bir değişkeni tanımlamanın üç farklı yolu nelerdir?
* Hangi birini ne zaman kullanmalısınız?
* Değişkenler için adlandırma kuralları nelerdir?
* Operatörler, işlem yapılandırıcıları ve işlemler nelerdir?
* Birleştirme nedir ve sayıları ve dizeleri birleştirirken ne olur?
* JavaScript'teki farklı operatör türleri nelerdir?
* == ve === arasındaki fark nedir?
* Operatör öncelik değerleri nelerdir?
* Artırma / azaltma operatörleri nelerdir?
* Bunları öne eklemenin ve sonuna eklemenin farkı nedir?
* Atama operatörleri nelerdir?
* Unary Plus Operator nedir?

### JavaScript Kodunu Nasıl Çalıştırılır?

Fundamentals kursunun çoğunda yazacağımız tüm JavaScript, tarayıcı üzerinden çalıştırılacaktır. Fundamentals ve NodeJS yolu sonraki derslerinde JavaScript'i tarayıcı ortamının dışında nasıl çalıştıracağınızı gösterecektir. Bu derslerin dışında, şimdilik istisna belirtilmedikçe JavaScript'inizi tarayıcıda çalıştırmaya her zaman varsaymalısınız, aksi takdirde beklenmedik hatalarla karşılaşabilirsiniz.

Başlamak için, JavaScript kodunu içinde barındıran bir HTML dosyası oluşturmanız yeterlidir. Bilgisayarınızda herhangi bir dosyaya temel HTML iskeletini yazın:

~~~html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Sayfa Başlığı</title>
</head>
<body>
  <script>
    // JavaScript'inizi buraya yazın!
    console.log("Merhaba, Dünya!")
  </script>
</body>
</html>
~~~

Bu dosyayı kaydedin ve bir web tarayıcısında açın (bunu yapmak için Visual Studio Code'daki ["Live Server"](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) özelliğini kullanabilirsiniz!) ve daha sonra <span id="access-devTools-console">boş web sayfasına sağ tıklayıp "İncele" veya "Öğeyi İncele" seçeneğini seçerek tarayıcının konsolunu açın. 'Geliştirici Araçları' panelinde 'Konsol' sekmesini bulun ve seçin</span>, burada `console.log` ifadesinin çıktısını görmelisiniz.

> <span id="console-log">`console.log()` tarayıcınızın geliştirici konsoluna bir şey yazdırmak için kullanılan komuttur. Bu, bu ve gelecekteki tüm makalelerin ve egzersizlerin sonuçlarını konsoldan yazdırmak için kullanabilirsiniz.</span> Bu ve gelecekteki derslerdeki tüm örneklerle birlikte kod yazmanızı öneririz.

Bir web sayfasına JavaScript dahil etmenin başka bir yolu, harici bir betiği içermektir. Bu, web sitenize harici CSS dokümanlarını bağlamakla çok benzerdir.

~~~html
  <script src="javascript.js"></script>
~~~

JavaScript dosyaları, stiller için `.css`'ye benzer şekilde `.js` uzantısına sahiptir. Harici JavaScript dosyaları, daha karmaşık betikler için kullanılır.

### Değişkenler

Değişkenleri, kodunuzdaki veriler için sadece "depolama konteynerleri" olarak düşünebilirsiniz. <span id="variable-declaration">Yakın zamana kadar, JavaScript'te bir değişken oluşturmanın tek yolu `var` ifadesiydi. Ancak, en yeni JavaScript sürümlerinde iki yol daha var: `let` ve `const`.</span>

1. [Bu değişken öğreticisi](http://javascript.info/variables) ihtiyacınız olan her şeyi açıklar! Sonunda __Görevler__ bölümünü yapmayı unutmayın. Pratik yapmadan bilgi pekişmez!

Yukarıdaki öğretici bunu belirtse de, tekrar belirtmek önemlidir: `let` ve `const`, JavaScript'te değişkenleri tanımlamanın nispeten yeni yollarıdır. <span id="avoid-var">İnternetin birçok yerinde _birçok_ öğreticide (ve kodda) `var` ifadeleriyle karşılaşmanız muhtemeldir. Bu sizi rahatsız etmesine izin vermeyin! `var`'ın doğasında yanlış bir şey yoktur ve çoğu durumda `var` ve `let` aynı şekilde davranır. Ancak, bazen `var`'ın davranışı beklediğiniz gibi değildir. Şimdilik sadece `let` (ve `const`) kullanın.</span>

### Sayılar

Sayılar, programlama mantığının yapı taşlarıdır! Aslında, en azından biraz temel matematik içermeyen herhangi bir yararlı programlama görevi düşünmek zordur... bu yüzden sayıların nasıl çalıştığını bilmek açıkça önemlidir. Neyse ki, oldukça basittir.

1. [Bu W3Schools dersi](https://www.w3schools.com/js/js_arithmetic.asp) ve ardından [bu ders](https://www.w3schools.com/js/js_numbers.asp), JavaScript'te sayılarla neler yapabileceğinize iyi bir giriş yapar.
2. [Bu MDN makalesi](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math), temel matematiği JavaScript'te nasıl uygulayacağınızı öğretirken farklı bir bakış açısından aynı bilgileri kapsar. Sayılarla yapabileceğiniz çok daha fazlası var, ancak şimdilik bunların hepsi ihtiyacınız olanlar.
3. JavaScript'te sayılarla (diğer şeyler arasında!) ne yapabileceğinizi oldukça iyi bir şekilde gösteren [bu makaleyi](http://javascript.info/operators) okuyun (ve kodla birlikte çalışın). Sayılarla neler yapabileceğinize dair oldukça iyi bir fikir edineceksiniz.


### Görev

<div class="lesson-content__panel" markdown="1">
Aşağıdaki egzersizleri deneyin (ve `console.log()` kullanmayı unutmayın!):

1. İki sayıyı toplayın! (html dosyanızda `console.log(23 + 97)` yazın)
2. Farklı 6 sayı dizisini bir araya getirin.
3. Aşağıdaki denklemi çözümleyin: `(4 + 6 + 9) / 77`
    * Cevap yaklaşık `0.24675` olmalıdır.
4. Hadi değişkenleri kullanalım!
    * Script etiketinin üstüne şu ifadeyi yazın: `let a = 10`
    * Konsola `console.log(a)` yazarsanız `10` yazısı gelmelidir.
    * Konsolda şunu deneyin: `9 * a`
    * ve bunu: `let b = 7 * a` ( `undefined` \* değerini döndürür) ve sonra `console.log(b)` yazın.
5. Şimdiye kadar bu işi halletmeye başladınız... şunu deneyin:
    * Sabit bir değişken olan `max`ı `57` değeriyle belirtin.
    * Başka bir değişken olan `actual`ı `max - 13` olarak ayarlayın.
    * Başka bir değişken olan `percentage`i `actual / max` olarak ayarlayın.
    * Eğer konsola `percentage` yazarsanız ve enter tuşuna basarsanız `0.7719` gibi bir değer göreceksiniz.
6. Script etiketinizde çeşitli şeylerle oynamaya birkaç dakika daha ayırın. Sonunda, bu sayıların ve şeylerin gerçekten web sayfasında görünmesini nasıl yapacağımızı öğreneceğiz, ancak tüm bu mantık aynı kalacak, bu nedenle devam etmeden önce rahat olduğunuzdan emin olun.

_* Javascript kodunu konsolda çalıştırarak fark ettiğiniz gibi, konsol, yürüttüğü kodun sonucunu yazdırır (döndürme deyimi denir). Bu konuda daha fazla bilgiyi sonraki derslerde öğreneceksiniz, ancak şimdilik bir atama ile deklarasyon (örneğin `let b = 7 * a`) `undefined` değerini döndürür, bu nedenle bir değişkene bir değer atayamaz ve aynı satırda değerini okuyamazsınız._
</div>

### Ek Kaynaklar

Bu bölüm, diğer içeriklere yardımcı olan faydalı bağlantılar içerir. Gereksiz değildir, bu yüzden ek olarak düşünün.

* `var` ve `let` arasındaki kesin farklar [javascript.info](https://javascript.info/var) adresinde açıklanmaktadır.

### Bilgi Kontrolü

Bu bölüm, bu derste kendi anlayışınızı kontrol etmeniz için sorular içerir. Bir soruyu yanıtlayamıyorsanız, tıklayın ve bağlantı verilen materyali gözden geçirin.

* [Bir değişkeni deklare etmek için üç yolun adını verin](#variable-declaration)
* [Üç değişken bildiriminden kaçınmalı mısınız ve neden?](#avoid-var)
* [Değişkenleri nasıl adlandırmanız gerektiği hakkında hangi kuralları izlemelisiniz?](https://javascript.info/variables#variable-naming)
* [Sayıları ve dizeleri bir araya getirdiğinizde ne olur?](https://javascript.info/operators#string-concatenation-with-binary)
* [Modulo (%), veya Kalan, operatörü nasıl çalışır?](https://javascript.info/operators#remainder)
* [`==` ve `===` arasındaki farkı açıklayın.](https://www.w3schools.com/js/js_numbers.asp)
* [Ne zaman `NaN` sonucu alırsınız?](https://www.w3schools.com/js/js_numbers.asp)
* [Bir sayıyı nasıl artırır veya azaltırsınız?](https://javascript.info/operators#increment-decrement)
* [Ön ekli ve son ekli artırım/azaltım operatörleri arasındaki fark nedir?](https://javascript.info/operators#increment-decrement)
* [Operatör önceliği nedir ve JS'de nasıl ele alınır?](https://javascript.info/operators#operator-precedence)
* [Geliştirici araçlarına ve konsola nasıl erişilir?](#access-devTools-console)
* [Bilgileri konsola nasıl kaydederiz?](#console-log)
* [Karakteristik bir sayıdaki dize temsili için artı işleyicisi ne yapar? örn. +"10"](https://javascript.info/operators#numeric-conversion-unary)