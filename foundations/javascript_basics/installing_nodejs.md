### Giriş

Node.js, JavaScript'i web tarayıcınızın dışında çalıştırmanıza olanak tanıyan bir JavaScript çalışma ortamıdır. Yaklaşan derslerde bazı alıştırmalar için buna ihtiyacımız olacak. Başlamadan önce, sisteminize Node'yi kurabilmemiz için ihtiyacımız olan bazı gerekli araçlar var.

`nvm` (Node Sürüm Yöneticisi) kullanarak kurulum yapacağız, çünkü Node sürümlerini değiştirmeyi ve Node'yi yükseltmeyi kolaylaştırır. JavaScript ortamlarında kullanılan çeşitli kütüphaneleri ve araçları kurmak için daha sonra kullanacağımız `npm` adında başka bir araç var. Bu ikisini karıştırmak kolay olabilir, bu yüzden dikkatli okuyun!

Node'u nvm kullanarak kurmak da çok kolay, bu yüzden bu hızlıca halledilmeli :)

### Ders Genel Bakışı

Bu bölüm, bu ders boyunca öğreneceğiniz konuların genel bir özetini içerir.

- `nvm` (Node Sürüm Yöneticisi) ve `npm` nasıl kurulacağını öğrenin.
- Node konsolunu nasıl çalıştıracağınızı öğrenin.

### NVM Kurulumu

<details markdown="block">
  <summary class="dropDown-header">Linux Üzerinde Kurulum</summary>

#### Adım 0: Ön Koşullar

nvm'yi düzgün bir şekilde kurmak için `curl`'e ihtiyacınız olacak. `curl`'ü kurmak için aşağıdaki komutu çalıştırın:

```bash
sudo apt install curl
```

Not: Curl kurulumunun tamamlanması için Ubuntu paket listelerini en son sürüme güncellemeniz gerekebilir. Eğer öyleyse, aşağıdaki komutu çalıştırın:

```bash
sudo apt update && sudo apt upgrade
```

#### Adım 1: NVM'yi İndirme ve Kurma

`nvm`'yi kurmak için bu komutu çalıştırın:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

#### Adım 2: NVM'yi Başlatma

Terminalde `nvm`'yi nasıl başlatacağınıza dair bazı yönergeler olmalı. Eğer yoksa, (veya terminalden kopyalamak istemiyorsanız), bu komutları çalıştırın:

```bash
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # Bu, nvm'yi yükler
```

`nvm`'nin kurulduğunu şu komutu çalıştırarak doğrulayabilirsiniz:

```bash
command -v nvm
```

Eğer bu `nvm: komut bulunamadı` döndürürse, terminali kapatın ve yeniden açın.

</details>

<details markdown="block">
  <summary class="dropDown-header">macOS Üzerinde Kurulum</summary>
  
macOS 10.15 ve üzeri sürümlerde, varsayılan kabuk artık zsh'dir. Kurulum sırasında, nvm kullanıcı ana dizininde bir `.zshrc` dosyası arayacaktır. Varsayılan olarak, bu dosya mevcut değildir, bu yüzden onu oluşturmamız gerekiyor.

`.zshrc` dosyasını oluşturmak ve nvm kurulumuna başlamak için aşağıdaki komutları çalıştırın:

```bash
touch ~/.zshrc
```

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

Terminalinizi yeniden başlat

ın, veya aşağıdakileri terminalinize kopyalayıp yapıştırın ve <kbd>Enter</kbd>'a basın:

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # Bu, nvm'yi yükler
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # Bu, nvm bash_completion'ı yükler
```

nvm kurulumunuzu test etmek için:

```bash
nvm --version
```

Daha fazla bilgi için, [NVM'in GitHub Dokümantasyonu](https://github.com/nvm-sh/nvm#installation-and-update)'na bakın.

</details>

### Node Kurulumu

Artık `nvm`'yi kurduğumuza göre, Node'yi kurabiliriz.

#### Adım 1: Kurulum

Çalıştırın:

```bash
nvm install --lts
```

Bu, Node'un 'uzun süreli destek' (LTS) olan en son stabil sürümünü kuracak ve terminalde çok sayıda çıktı göreceksiniz. Her şey yolunda gittiyse, çıktının satırları arasında (X'ler gerçek numaralarla değiştirilmiş olarak) aşağıdakine benzer bir şey görmelisiniz:

```bash
Downloading and installing Node vXX.xx.x...
```

Eğer öyle değilse, terminali kapatın, yeniden açın ve `nvm install --lts` komutunu tekrar çalıştırın.

#### Adım 2: Node Sürümünü Ayarlama

`node` komutunu çalıştırdığımızda hangi Node sürümünü kullanacağımızı `nvm`'ye söylememiz gerekiyor. Bu çok kolay; sadece aşağıdaki komutu çalıştırın:

```bash
nvm use --lts
```

Bilgisayarımızda kurulu olan en son LTS sürümü Node'u kullanması için `nvm`'ye talimat verdik. Gelecekteki derslerde kuracağımız paketlerle uyumsuzlukları önlemek için Node'un LTS sürümünü **mutlaka** kullanmalısınız. Node'un LTS sürümü, ilk yayınlandıktan sonra otuz ay boyunca destek garantisi verilen bir sürümdür. Çeşitli paketlerle daha stabil ve uyumlu olduğundan, LTS olmayan bir Node sürümünden daha fazladır.

Şimdi `node -v` komutunu çalıştırdığınızda, `vXX.xx.x` veya benzer bir şey görmelisiniz (X'ler gerçek numaralarla değiştirilmiş olarak).

Bunu gördüyseniz, Node'u başarıyla kurmuşsunuz demektir!

### Node Konsolunu Kullanma

Kolaylık sağlamak adına, Node, IRB için ruby'ye benzer şekilde, JavaScript kodunuzu doğrudan terminalinizde çalıştırmanıza ve düzenlemenize olanak tanıyan etkileşimli bir konsol sağlar. Bu, her seferinde tarayıcıyı açmadan kodunuzun küçük parçalarını hızlı bir şekilde hata ayıklamak veya test etmek için oldukça yararlıdır.

Node konsolunu çalıştırmak için, terminalinizi açın ve `node` yazın. Konsoldan çıkmak için `.exit` yazın.

### Ek Kaynaklar

Bu bölüm, ilgili içeriğe yardımcı olabilecek bağlantılar içerir. Gerekli değildir, bu yüzden bunu ek olarak düşünün.

- Görünüşe göre bu ders henüz ek kaynaklara sahip değil. Kürümüze katkıda bulunarak bu bölümü genişletmemize yardımcı olun.