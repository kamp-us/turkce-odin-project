### Giriş

Geliştiriciler kod yazmaktan daha çok kod okumaya zaman harcıyorlar. Bu kendi kodunuzda bile doğrudur.Lütfen kendinize ve kodunuzu kullanacak,bakımını yapacak ve geliştirecek kişilere iyilik yapmak için okunabilir kod yazmayı öğrenin.

### Derse Genel Bakış

Bu bölüm, bu derste öğreneceğiniz konuların genel bir özetini içermektedir.

- Okuması zor ile okuması kolay kod arasındaki farkı nasıl ayırt edebilirim?
- Kodunuzu daha temiz hale getirmek için programlama prensiplerini kullanın.
- İyi yorumlar yazın.

### Temiz Kod Yazma

Aşağıdaki iki JavaScript kod parçasını inceleyin:

Bu okuması zor ve kötü görünen bir kod örneği:

~~~JavaScript
const x =
function(z) {
let w = 0;z.forEach(
function(q){
     w += q;
});return w;
};

x([2, 2, 2]);
~~~

Şimdi bu temiz ve okuması kolay bir kod örneği:

~~~JavaScript
const sumArray = function(array) {
  let sum = 0;
  array.forEach(function(number) {
    sum += number;
  });
  return sum;
};

sumArray([2, 2, 2]);
~~~

İnanın veya inanmayın, her iki fonksiyon da aynı şeyi\(tamamen aynı şekilde!\) yapıyor ve her ikisi de tamamen geçerli kodlar, ancak görüldüğü üzere ikincisini takip etmesi daha kolay.Başka birisiyle ortak bir projede çalıştığınızı ve ilk fonksiyonu yazdığını hayal edin.. İşinizi yapabilmeniz için ne olup bittiğini anlamalısınız, ilk örnekte bunun için ne kadar süre harcamanız gerekeceğini düşünün. Kendi projenizi yazarken ilk fonksiyonu bir veya iki hafta önce yazdığınızı ve tek başınıza çalıştığınızı düşünün. Tam olarak ne yaptığınızı muhtemelen hatırlamayacaksınız. Her şeyi çözmek ve anlamak için tekrar iyi bir zaman harcamanız gerekecektir.

Gerçekten ikincisini takip etmek çok daha kolaydır. Kodun içerisindeki her şeyi tam olarak anlamasanız bile değişkenler açıkça isimlendirildiği için tahmin edebilirsiniz. Girintinin tutarlı kullanımı da fonksiyonun farklı bölümlerini anlaşılabilir kılmaktadır.

Harika bir JavaScript kodunu oluşturma yöntemleri hakkında birçok farklı görüş var. En önemli şey sadece tutarlı olmanızdır. Kodları girintilemek için tab kullanan ve boşluk kullanan kullanıcılar arasındaki savaş o kadar derinleşti ki [bu aslında artık bir şaka](https://www.youtube.com/watch?v=SsoOG6ZeyUI), ancak tutarlı olduğunuz sürece gerçekten hangisini tercih ettiğiniz önemli değil.

### Kurallar veya Kılavuzlar

1.  Girintileme: Kullandığınız girintileme stili gerçekten önemli değil. Farklı JS stil rehberleri farklı seçenekleri önerebilir ve biri diğerinden üstün değildir. Her halükarda önemli olan tutarlılıktır. Alıştırmalarımızda girintileme için 2 boşluk kullanacağız.

2.  Noktalı virgüller: Noktalı virgüller, JavaScript'te çoğunlukla isteğe bağlıdır. Çünkü JS derleyicisi atlanmışlarsa otomatik olarak ekleyecektir. Fakat bu fonksiyonalite bazı durumlarda bozulabilir ve kodunuzda hatalara neden olabilir. Bu yüzden noktalı virgülü eklemeye alışmak daha iyidir. Yapmanız gereken sadece eklemek!

3. Satır uzunluğu: Yine farklı stil rehberleri bu konuda farklı önerilerde bulunabilir, ancak neredeyse tümü her satır uzunluğunu sınırlandırmayı önerir. Bu kural diğer kurallar kadar sıkı değildir. Fakat genel bir kural olarak, kodunuzun her satırı yaklaşık 80 karakterden sonra manuel olarak bölmeniz kodunuzu daha okunaklı hale getirir. Birçok kod düzenleyecisi, bu eşii geçtiğinizde size uyarı verecek bir satır göstergesine sahiptir. Satırları manuel olarak bölerken, operatör veya virgülün hemen sonrasında bölmeniz önerilir. Örneğin şunları yapabilirsiniz:

   - devam satırlarını aynı seviye girintiyle girintileyin,
   - devam eden satırları dikey olarak ilk değişkenle hizalayın,
   - veya tamamen farklı bir biçim kullanabilirsiniz. Kurallar katı değildir ve iş ortamından iş ortamına değişkenlik gösterebilir, yine de tutarlı olmaya dikkat edin.

   ~~~javascript
   // Olası bir format:
   let reallyReallyLongLine =
     something +
     somethingElse +
     anotherThing +
     howManyTacos +
     oneMoreReallyLongThing;

   // Diğer olası bir format:
   let anotherReallyReallyLongLine = something + somethingElse + anotherThing +
                                     howManyTacos + oneMoreReallyLongThing;
   ~~~
   
   ​

4.  Fonksiyonları ve Değişkenleri isimlendirme: Fonksiyonlar ve değişkenler için isimlendirme açık olmalıdır. Her zaman camelCase kullanın. Tutarlılık ve okunabilirlik için değişkenler her zaman bir isim veya sıfatla(yani bir isim öbeğiyle) başlamalı ve fonksiyonlar bir fiil ile başlamalıdır. Döngü veya callback fonksiyonu bağlamında tek karakterli değişken adları kullanmak sorun değil ama başka yerlerde kullanmamaya özen gösterin.

    ~~~javascript
    // İyi
    const numberOfThings = 10;
    const myName = "Thor";
    const selected = true;

    // Kötü (bu örnekte değişken isimleri fiillerle başladığı için fonksiyonlarla karıştırılabilir)
    const getCount = 10;
    const isSelected = true;

    // İyi 
    function getCount() {
      return numberOfThings;
    }

    // Kötü (bu örnekte fonksiyon bir isimdir)
    function myName() {
      return "Thor";
    }
    ~~~


### Ödev

<div class="lesson-content__panel" markdown="1">

1.  [Bu temiz kod ipuçlarının listesi](https://onextrapixel.com/10-principles-for-keeping-your-programming-code-clean/).
2.  [Makale](https://blog.codinghorror.com/coding-without-comments/), [Diğer makale](https://blog.codinghorror.com/code-tells-you-how-comments-tell-you-why/) kodunuzda yorumların rolü içi bu makalelere göz atabilirsiniz.
</div>

### Bilgi ölçme

Bu bölüm temiz kod yazma dersinde anladığınızı kendi kendinize kontrol etmek için sorular içermektedir. Bir soruyu cevaplamakta zorlanıyorsanız, üzerine tıklamanız ve bağlantıda verilen materyale göz atmanız önerilir.

- [Temiz kod yazmak neden önemli?](#writing-clean-code)
- [Önceden bahsedilen 5 temiz kod yazma prensibini adlandırın.](https://onextrapixel.com/10-principles-for-keeping-your-programming-code-clean/)
- [İyi yorumlar ve kötü yorumların farklılıkları nedir?](https://onextrapixel.com/10-principles-for-keeping-your-programming-code-clean/)

### Ek Kaynaklar

Bu bölüm, ilgili içeriğe yönlendiren yararlı bağlantılar içerir. Zorunlu değildir, dolayısıyla ek olarak düşünülebilir.

* [Güzel bir görüş yazısı](https://www.martinfowler.com/bliki/CodeAsDocumentation.html)
* ["Kendi kendini açıklayan kod" rehberi](http://wiki.c2.com/?SelfDocumentingCode)
* [Airbnb stil rehberi](https://github.com/airbnb/javascript)  
* [Cümleler yazmak için yöntem zincirleme](https://web.archive.org/web/20190211152543/https://javascriptissexy.com/beautiful-javascript-easily-create-chainable-cascading-methods-for-expressiveness/)   