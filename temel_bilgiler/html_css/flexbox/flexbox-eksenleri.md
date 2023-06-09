### Giriş

Bir flex konteynerindeki öğelerin yönünün `flex-direction` özelliği kullanılarak nasıl kontrol edilebileceğini görelim.

### Derse Genel Bakış

Bu bölüm, bu derste öğreneceğiniz konuların genel bir özetini içerir.

-   Bir flex konteynerinin 2 "eksenini" öğreneceksiniz.
-   İçeriğinizi satırlar yerine sütunlar halinde düzenlemek için eksenleri nasıl değiştireceğinizi öğreneceksiniz.

Flexbox ile ilgili en kafa karıştırıcı şey, yatay veya dikey olarak çalışabilmesi ve hangi yönde çalıştığınıza bağlı olarak bazı kuralların biraz değişmesidir.

Bir flex konteyneri için varsayılan yön yatay veya `row` (satır)dır, <span id='flex-vertical'>ancak yönü dikey veya `column` (sütun) olarak değiştirebilirsiniz. Yön, CSS'de şu şekilde belirtilebilir:
</span>

~~~css
.flex-container {
  flex-direction: column;
}
~~~

### Eksenler

<span id='flex-axes'>Hangi yönü kullanırsanız kullanın, flex konteynerinizin 2 eksene sahip olduğunu bilmeniz gerekmektedir: ana eksen ve çapraz eksen. `Flex-direction` değeri değiştirildiğinde, değişen şey bu eksenlerin yönüdür. _Çoğu durumda_, `flex-direction: row` ana ekseni yatay (soldan sağa) ve `column` ana ekseni dikey (yukarıdan aşağıya) yerleştirir.</span>

Yani ilk örneğimizde bir div üzerine `display: flex` koyduk ve çocuklarını yatay olarak sıraladı. Bu, varsayılan ayar olan "`flex-direction: row`ın bir gösterimidir. Aşağıdaki örnek çok benzer. `flex-direction: column` yazan satırın yorumunu kaldırırsanız, bu div'ler dikey olarak sıralanırlar.

<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="BaZKPdw" data-editable="true" data-user="TheOdinProjectExamples" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>[CodePen](https://codepen.io)'de TheOdinProject'in ([@TheOdinProjectExamples](https://codepen.io/TheOdinProjectExamples)) yazdığı [flex-direction örneğine](https://codepen.io/TheOdinProjectExamples/pen/BaZKPdw) bakın.
  </span> 
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Unutulmaması gereken bir nokta, bu örnekte, `flex: 1` kısaltmasını kullanırsak `flex-direction: column` beklendiği gibi çalışmaz. Şimdi deneyin (yani, `flex: 1 1 auto;` satırındaki flex değerini değiştirin). `flex: 1` kullanılırsa neden çalışmadığını anlayabilir misiniz? Orada _açıkça_ tanımlanmış bir `yüksekliğe` sahip olmalarına rağmen div'ler çöker.

Bunun nedeni, <span id='row-flex-basis'> flex kısaltmasının `flex-basis`ı `0`a genişletmesidir; bu, tüm `flex-grow` ve `flex-shrink`nin hesaplamalarına `0`dan başlayacağı anlamına gelir.</span> Boş div'lerin varsayılan olarak 0 yüksekliği vardır, bu nedenle flex öğelerimizin kaplarının yüksekliğini doldurması için aslında herhangi bir yüksekliğe sahip olmaları gerekmez.

Yukarıdaki örnek, `flex: 1 1 auto` belirterek ve flex öğelerin varsayılan `height` değerlerinin verilmesi söylenerek bu düzeltildi. Ebeveyn `.flex-container` elementinin üzerine bir yükseklik koyarak veya kısaltma yerine `flex-grow: 1` kullanarak da düzeltebilirdik.

Dikkat edilmesi gereken başka bir ayrıntı: <span id='column-flex-basis'>flex-direction'u `column` olarak değiştirdiğimizde, `flex-basis`, `width` yerine `height` anlamına gelir.</span> Bağlam göz önüne alındığında bu bariz olabilir, ancak dikkat edilmesi gereken bir şeydir.

Konudan biraz saptık... flex-direction ve eksenlerden bahsediyorduk. Önemli olan kısım, varsayılan davranış, her şeyi yatay olarak düzenleyen `flex-direction: row` şeklindedir. Bunun genellikle CSS'deki diğer ayrıntıları değiştirmeden iyi çalışmasının nedeni, blok düzeyindeki öğelerin varsayılan olarak ebeveynlerinin tam genişliğine sahip olmasıdır. `flex-direction: column` kullanarak her şeyi dikey olarak değiştirmek karmaşıklık katar çünkü blok düzeyindeki öğeler varsayılan olarak içeriklerinin yüksekliğine göre ayarlanır ve bu durumda içerik yoktur.

> Yukarıdan aşağıya veya sağdan sola yazılan bir dil kullanıyorsanız, flex-direction davranışının değişebileceği durumlar vardır, ancak Arapça veya İbranice bir web sitesi yapmaya hazır olana kadar bunun için endişelenmemelisiniz. 

Eksenlerin flexbox ile nasıl çalıştığına dair etkileşimli bir demo için şu Scrim'e göz atın:

<iframe src="https://scrimba.com/learn/flexbox/main-axis-and-cross-axis-flexbox-tutorial-cz94MT8?embed=odin,mini-header,no-big-play,no-next-up" sandbox="allow-scripts allow-same-origin" width="100%" height="400"></iframe>

### Bilgi Ölçme

Bu bölüm, bu dersi anlayıp anlamadığınızı kendi başınıza kontrol etmeniz için sorular içermektedir. Bir soruyu yanıtlamakta sorun yaşıyorsanız, soruya tıklayın ve bağlantının verdiği materyali inceleyin.

-   [Flex öğelerin yatay yerine dikey olarak düzenlenmesini nasıl sağlarsınız?](#flex-vertical)
-   [Bir `column` flex-container'da, `flex-basis` neyi ifade eder?](#column-flex-basis)
-   [Bir `row` flex-container'da, `flex-basis` neyi ifade eder?](#row-flex-basis)
-   [Önceki iki sorunun neden farklı yanıtları var?](#flex-axes)

### Ek Kaynaklar

Bu alanda içerikle alakalı faydalı linkler bulunmaktadır. Zorunlu değildir, ek olarak düşünülmelidir.

*   [Bu flexbox cheatsheet](https://flexbox.malven.co/)'i, flex ve özellikleri için bazı faydalı kaynaklara sahiptir.
