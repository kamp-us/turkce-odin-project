### Giriş

Bu projede, portgolyonuza koyabileceğiniz ve DOM manipülasyonu becerilerinizi geliştirecek oldukça iyi bir oyuncak oluşturacaksınız. Bir eskiz defteri ve manyetik çizim tahtasının tarayıcı versiyonunu inşa edeceksiniz.

Bu proje sizin için kolay _olmamalı_. Doğru JavaScript metodlarını ve kullanılacak CSS kodlarını bulabilmek için bolca Google'ı kullanacaksınız -aslında, amaç bu! Daha önce öğrendiğiniz araçlarla bu projeyi _yapabilirsiniz_ ve eğer ihtiyacınız olduğunu düşünüyorsanız daha değinmediğimiz bir çok konuyu internetten öğrenebileceğiniz çokça kaynak var. Size ilk adımlarda rehberlik edeceğiz fakat bunları uygulamak size kalmış.

Eğer gerçekten takılı kaldıysanız, sohbet odasına uğrayın. Oradaki biri size doğru yönü gösterecektir.

### Ödev

<div class="lesson-content__panel" markdown="1">
Sık sık ve erkenden commit etmeyi unutmayın! Commit Mesajları dersini buradan hatırlayabilirsiniz](https://www.theodinproject.com/paths/foundations/courses/foundations/lessons/commit-messages)!

1.  Bu projeye ait Git deposu kurmak için [Odin'in Tarifleri projesinin üstündeki talimatları izleyin](https://www.theodinproject.com/paths/foundations/courses/foundations/lessons/recipes#setting-up-your-projects-github-repository).
2.  16x16 kare div'lerden oluşan bir ızgara içeren web sayfası oluşturun.
    *   JavaScript kullanarak div'leri oluşturun. HTML dosyanızda kopyala yapıştır yaparak bunları elle oluşturmaya çalışmayın!
    *   Izgara karelerinizi başka bir "kapsayıcı" div'in içine koymak en iyisidir \(böylece doğrudan HTML'nize eklenebilir\).
    *   Div'lerin bir ızgara olarak \(her satırda yalnızca bir tane olması yerine\)  görünmesini sağlamalısınız. Bu, flexbox hakkında öğrendiklerinizi uygulamak için mükemmel bir fırsat.
    *   Karelerin boyutuna etki edebildikleri için border'lara (kenar çizgilerine) ve margin'lere (dış kenar boşluklarına) dikkat edin!
    *   "Aman Tanrım, neden ızgaram oluşturulmuyor ???"
        *   CSS stil sayfanızı bağladınız mı?
        *   Tarayıcınızın geliştirici araçlarını açın.
        *   JavaScript konsolunda herhangi bir hata olup olmadığını kontrol edin.
        *   Öğelerin gerçekten görünüp görünmediğini ancak bir şekilde gizlenip gizlenmediğini görmek için "öğeler" bölmenizi kontrol edin.
        *   İster istemez gidin ve gerçekten yüklenip yüklenmediğini görmek için JavaScript'inize `console.log` ifadeleri ekleyin.
3.  Fareniz üzerlerinden geçtiğinde ızgara div'lerinin renk değiştirmesi ve ızgaranızda kalem gibi bir \(pikselleştirilmiş\) iz bırakması için bir "hover" efekti ayarlayın.
    *   İpucu: "Hovering", fareniz bir div'e girdiğinde gerçekleşen ve fareniz div'den ayrıldığında biten şeydir. Başlangıç noktası olarak bu olaylardan herhangi biri için olay dinleyicileri ayarlayabilirsiniz.
    *   Aşağıdakiler de dahil olmak üzere div'lerin rengini değiştirmenin birden çok yolu vardır:
        *   div'e yeni bir sınıf eklemek.
        *   JavaScript kullanarak div'in arka plan rengini değiştirme.
4.  Ekranın üst kısmına bir düğme ekleyin. Kullanıcıya yeni ızgara için kenar başına kare sayısını soran bir açılır pencere oluştursun. Kare sayısı girildikten sonra mevcut ızgara kaldırılmalı ve yeni bir eskiz defteriniz olması için _önceki ile aynı alanda_ \(örn. 960 piksel genişliğinde\) yeni bir ızgara oluşturulmalıdır. **İpucu**: Kullanıcı girişi sınırını maksimum 100 olarak ayarlayın. Daha fazla sayıda kare, daha fazla bilgisayar kaynağının kullanılmasına neden olarak potansiyel olarak önlemek istediğimiz gecikmelere, donmalara veya çökmelere neden olur.
    *   HTML'deki `button (düğme)` etiketlerini ve bir JavaScript işlevinin tıklandığında çalışmasını nasıl sağlayabileceğinizi araştırın.
    *   Ayrıca `prompt (diyalog kutusu)`na da bakın.
    *   Örneğin diyaloğa "64" girebilmeniz ve kullanılan toplam piksel miktarını değiştirmeden yepyeni bir 64x64 ızgarasının açılabilmesi gerekir.
5.  Projenizi GitHub'a aktarın!

#### Ekstra Kredi
Bir dizi değişiklik yaparak fareyle etkileşim kurarken bir karenin davranışını dönüştürün.

1. Siyahtan beyaza basit bir renk değişikliği yerine her etkileşim karenin RGB (Kırmızı Yeşil Mavi) değerini tamamen rastgele hale getirmelidir. 
2. Ek olarak, her etkileşimin kareye %10 daha fazla siyah veya renk eklediği aşamalı bir karartma efekti uygulayın. Amaç, yalnızca on etkileşimden sonra tamamen siyah bir kare elde etmektir.

Bu meydan okumalardan birini veya her ikisini birden yapmayı seçebilirsiniz, bu size kalmış.
</div>