# Python_Ta-Lib_for_Mac
## Python Ta-Lib Kütüphanesi Yükleme Sorunu Çözümü | Mac / Macbook M2

Merhaba Arkadaşlar, 

Macbook M2 kullanıcısıysanız ve Ta-lib kütüphanesini Python dosyasınıza ekleyemiyorsanız aşağıdaki adımları takip ederek yükleme işlemini yapabilirsiniz.

Öncelikle sisteminizde Home-brew yüklü olması gerekmektedir.
Home-brew’i yüklemek için terminale aşağıdaki komudu girmeniz gerekmektedir.

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Yükleme işlemini yaparken bilgisayarınızda şifreniz varsa şifrenizi isteyebilir. Şifrenizi terminal ekranına girerken ekranda metin veya  “*” işareti gibi bir ifade görmemeniz normaldir. Şifrenizi eksiksiz girdikten sonra **ENTER** tuşuna basınız. 

Terminalde karşınıza aşağıdaki şekilde bir ifade çıkacaktır.

    ==> This script will install:
    /opt/homebrew/bin/brew
    /opt/homebrew/share/doc/homebrew
    /opt/homebrew/share/man/man1/brew.1
    /opt/homebrew/share/zsh/site-functions/_brew
    /opt/homebrew/etc/bash_completion.d/brew
    /opt/homebrew

    Press RETURN/ENTER to continue or any other key to abort: 

Burada **ENTER** tuşuna basarak işlemi devam ettiriniz. 
Home-brew dosyaları otomatik olarak kütüphanenize eklenecektir. 

### DİKKAT!
Dosyaların yüklenmesi **“brew”** komutunu terminalde çalıştırabileceksiniz anlamına gelmez. 
Gerekli adımları uygulamadan terminale **“brew”** komutunu girerseniz aşağıdaki hata ile karşılaşabilirsiniz. 

    zsh: command not found: brew

Bu hatanın çözümü ve terminalde **“brew”** komutunu çalıştırmak için terminale sırasıyla aşağıdaki komutları girmeniz gerekmektedir.

    (echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/hnr/.zprofile

    eval "$(/opt/homebrew/bin/brew shellenv)"

**Tebrikler!** Artık **“brew”** komutunu terminalde çalıştırabilirsiniz. 

Şimdi Ta-Lib kütüphanesini eklemek için terminale aşağıdaki komutu giriniz!

    brew install ta-lib

**Tebrikler!** Ta-Lib kütüphanesi sisteminize yüklenmiştir.

### DİKKAT!
Python'da ta-lib kütüphanesini kullanabilmek için Python bağlantılarını (bindings) yüklemeniz gerekebilir. Bağlantıları aşağıdaki komutla yükleyebilirsiniz:

    pip install TA-Lib

Python bağlantılarını yükledikten sonra, **mport talib** ifadesini kullanarak kütüphaneyi Python projenize dahil edebilirsiniz.

Umarım bu yazı sayesinde sorununuzu çözmüş olursunuz. 

Eksiklik veya hata gördüğünüz bir yer olursa lütfen benimle iletişime geçin.

İyi günler dilerim.

