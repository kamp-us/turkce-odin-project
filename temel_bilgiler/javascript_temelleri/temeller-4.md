### Derse Genel Bakış

Bu bölüm, bu derste öğreneceğiniz konuların genel bir özetini içerir.

* Dizileri(arrays) kullanma.
* Yerleşik dizi yöntemlerini kullanma.
* Döngüleri kullanma.
* TDD alıştırmaları ile pratik yapma.

### Diziler

Dizeler ve sayılar yapı taşlarımız olabilir, ancak komut dosyalarınız daha karmaşık hale geldikçe, büyük miktarlarda bunlarla başa çıkmak için bir yola ihtiyacınız olacaktır. Neyse ki JavaScript tam da bu iş için kullanılan birkaç veri türüne sahiptir. Dizi, basitçe öğelerin (Dizeler, sayılar veya diğer şeyler) sıralı bir koleksiyonudur.

1. [Bu ingilizce eğitim](https://www.w3schools.com/js/js_arrays.asp) harika bir giriş niteliğindedir.
2. [Bu ingilizce makale](https://www.w3schools.com/js/js_array_methods.asp) en kullanışlı yerleşik dizi yöntemlerinden bazılarını kapsamaktadır. Bu temel bilgiler her gün kullanacağınız şeylerdir, bu yüzden çok fazla acele etmeyin ve kaçırmayın!
3. Bu ingilizce [Web Dev Simplified videosu](https://www.youtube.com/watch?v=7W4pQQ20nJg) JavaScript'teki dizilere genel bir bakışı yaklaşık 6 dakikada açıklıyor.

### Döngüler

Bilgisayarlar yorulmazlar ve gerçekten çok hızlıdırlar! Bu nedenle, hesaplamaların birden fazla kez yapılmasını gerektiren problemleri çözmek için çok uygundurlar. Bazı durumlarda, bir bilgisayar, bir insanın saatler sürebileceği bir görevi sadece birkaç saniye içinde _binlerce_ hatta _milyonlarca_ kez tekrarlayabilir. \(Açıkçası, buradaki hız hesaplamanın karmaşıklığına ve bilgisayarın hızına bağlıdır\). Bir bilgisayara tekrarlayan bir görev yaptırmanın bir yolu **döngü** kullanmaktır.

1. Bu ingilizce [MDN makalesini](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code) okuyun. Bu daha uzun bir makale, ancak sayfanın altındaki 'Active Learning' bölümlerini ele aldığınızdan emin olun.
2. Bir kez daha, aynı bilgi, [JavaScript.info](http://javascript.info/while-for)'dan biraz farklı içerik. \(Her şeyi bildiğinizi düşünüyorsanız bilgileri gözden geçirin, ancak **sayfanın sonundaki görevleri unutmayın**. En iyi _yaparak_ öğrenirsiniz.\)

### Test Odaklı Geliştirme

Test Odaklı Geliştirme \(TDD\), geliştirme dünyasında sıkça duyduğunuz bir ifadedir. Siz kodu gerçekten yazmadan önce kodunuzun nasıl çalışması gerektiğini açıklayan otomatik testler yazma pratiğini ifade eder. Örneğin, birkaç sayıyı toplayan bir işlev yazmak istiyorsanız, önce işlevi kullanan ve beklenen çıktıyı sağlayan bir test yazarsınız. Kodunuzu yazmadan önce test başarısız olacaktır ve test geçtiğinde kodunuzun doğru çalıştığını bilmeniz gerekir.

Birçok açıdan TDD, testler olmadan kod yazmaktan çok daha verimlidir. Yukarıdaki toplama fonksiyonu için testimiz olmasaydı, kodu kendimiz tekrar tekrar çalıştırmamız ve çalıştığından emin olana kadar farklı sayılar girmemiz gerekirdi... basit bir `add(2, 2)` için büyük bir sorun değil, ancak birisinin tic tac toe oyununu kazanıp kazanmadığını kontrol etmek gibi daha karmaşık fonksiyonlar için bunu yapmak zorunda olduğunuzu hayal edin: \(`game_win(["o", null, "x",null, "x",null, "x", "o", "o"])`). TDD yapmadıysanız, fonksiyonun doğru çalışıp çalışmadığını test etmek için kendinize karşı birden fazla oyun oynamanız gerekebilir!

Bu testleri gerçekten yazma sanatını size kursun ilerleyen bölümlerinde öğreteceğiz. Aşağıdaki alıştırmada testler sizin için zaten yazılmış durumda. Tek yapmanız gereken test ortamını kurmak, özellikleri okumak ve geçmelerini sağlayacak kodu yazmak!

### Ödev

<div class="lesson-content__panel" markdown="1">
Başlamak için aşağıdaki adımları takip edin. Adım 1'i tamamladıktan sonra, bunları doğru bir şekilde yapmak için **_her bir egzersiz_** için README'yi kullandığınızdan emin olun.

1. Dosyaları ve Jest'i [repository'nin README](https://github.com/TheOdinProject/javascript-exercises#readme)'sindeki talimatları dikkatlice izleyerek kurun.
2. Şimdi repository'i klonladığınıza ve Jest'i kurmak için `npm install` çalıştırdığınıza göre, bu alıştırmaları aşağıdaki sırayla tamamlayın:
    * helloWorld (Bu alıştırma, her şeyi düzgün bir şekilde kurduğunuzdan emin olmak için kasıtlı olarak çok basittir!)
    * repeatString
    * reverseString
    * removeFromArray
    * sumAll
    * leapYears
    * tempConversion
3. Çalışan bir çözüme sahip olduğunuzda, alıştırmanın verilen çözümüne kıyasla nasıl olduğunu görün. Alıştırmaların çözümleri her alıştırmanın 'solution' klasöründe bulunabilir.

</div>

### Ek Kaynaklar

Bu alanda içerikle alakalı faydalı linkler bulunmaktadır. Zorunlu değildir, ek olarak düşünülmelidir.

* Görünüşe göre bu dersin henüz herhangi bir ek kaynağı yok. Müfredatımıza katkıda bulunarak bu bölümü genişletmemize yardımcı olabilirsiniz.

### Bilgi Ölçme

Bu bölüm, bu dersi anlayıp anlamadığınızı kendi başınıza kontrol etmeniz için sorular içermektedir. Bir soruyu yanıtlamakta sorun yaşıyorsanız, soruya tıklayın ve bağlantının verdiği materyali inceleyin.

* [Dizi nedir?](https://www.w3schools.com/js/js_arrays.asp)
* [Diziler ne işe yarar?](https://www.w3schools.com/js/js_arrays.asp)
* [Bir dizi elemanına nasıl erişirsiniz?](https://www.w3schools.com/js/js_arrays.asp)
* [Bir dizi elemanını nasıl değiştirirsiniz?](https://www.w3schools.com/js/js_arrays.asp)
* [Bazı yararlı dizi özellikleri nelerdir?](https://www.w3schools.com/js/js_arrays.asp)
* [Bazı yararlı dizi yöntemleri nelerdir?](https://www.w3schools.com/js/js_array_methods.asp)
* [Döngüler ne işe yarar?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#why_bother)
* [Break deyimi nedir?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#exiting_loops_with_break)
* [Continue deyimi nedir?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code#skipping_iterations_with_continue)
* [Otomatik test yazmanın avantajı nedir?](#test-driven-development)