# Windows için Polymath

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**
(Her sohbette sessiz yapay zekâ ortağınız)

Polymath yanınızda oturur ve söz ya da bilgi eksikliğinde yardım eder. Karşınızdakinin ne söylediğini duyar, ekranınızda ne olduğunu görür ve bundan sonra ne yapacağınızı önerir. Onu başka kimse görmez ve asla sizin yerinize konuşmaz.

### Ne için gerekli

- **Dilini bilmediğiniz insanlarla konuşma.** Polymath karşınızdakini dinler ve ne dediğini gösterir. Sonra ne cevap vereceğinizi karşınızdakinin dilinde ve kendi ana dilinizde önerir (böylece ona tam olarak ne söylediğinizi her zaman anlarsınız). Çevirmenin arkasına saklanmak yerine konuşmanın içinde kendiniz kalırsınız.
- **Çevrim içi tanışma.** Polymath ekranınızı izleyebilir ve karşınızdakinin dilinde ve ana dilinizde nasıl cevap vereceğinizi önerebilir (böylece ona tam olarak ne yazdığınızı her zaman anlarsınız). Tam size benzeyen ama daha iyi bir mesaj yazarsınız.
- **Flört.** Cevap için bir fikri, bir şakayı ya da bir iltifatı tam ihtiyacınız olduğu anda alın.
- **Günlük işler.** Bir soru sorun, uygulamayla ekranın görüntüsünü alın ve tam olarak durumunuza uyan bir cevap alın.
- **Zor ve anlaşılmaz şeyler.** Nereye tıklayacağınızı ya da bir şeyin neden çalışmadığını bilmiyor musunuz? Ekranınızı Polymath'e gösterin, hatayı işaret edip nasıl düzelteceğinizi söylesin.

### Eskiden korkutan şeyler artık Polymath ile elinizin altında

- Çevrim içi iş görüşmesine girip ne söyleyeceğinizi bilmek.
- Google veya Meta'da reklam kurup bütçeyi boşa harcamamak.
- İlk web sitenizi yapıp herhangi bir hosting'e yüklemek.
- Kira veya kredi sözleşmesini anlayıp küçük puntolu maddeleri kaçırmamak.
- Vergi beyannamesini doldurmak veya vize başvurusu yapıp belgelerde hata yapmamak.
- Yabancı dilde de olsa dikkat çeken bir özgeçmiş ve ön yazı yazmak.
- Fiyat veya indirim konusunda anlaşmak, ev sahibiyle, ustayla ya da müşteriyle şartları konuşmak.
- Bankadan, vergi dairesinden veya sigortadan gelen mektubu anlayıp gerçekte sizden ne istendiğini öğrenmek.
- Hiçbir şey çalışmazken ve teknisyen pahalı ya da ulaşılamazken Wi-Fi modemini, yazıcıyı veya telefonu kurmak.
- Mağazaya, havayolu şirketine veya site yönetimine ikna edici bir şikâyet yazmak.
- Patronla, eşinizle veya ailenizle zor bir konuşmaya hazırlanıp doğru sözcükleri bulmak.

Eskiden bunun için yanınızda bir uzman ya da bir arkadaşa telefon gerekirdi. Şimdi her alanı bilen ve her zaman elinizin altında olan Polymath var.

---

Görüşmeler ve toplantılar için küçük bir yardımcı çubuk. Karşınızdaki kişiyi dinler ve sesini kendi dilinize çevirir, görüşme dilinde yanıt önerir, ekrandaki bir görevi çözer ve sohbette her soruya cevap verir.

**Çubuğu yalnızca siz görürsünüz.** Zoom, Teams, Meet, Discord ve OBS'de ekran paylaşırken, ekran görüntülerinde ve kayıtlarda görünmez.

## Özellikler

- **Listen** (`7` / `Ctrl` + `Alt` + `7`). Bilgisayarın sesini (görüşmede karşıdaki kişinin sesini) dinler, cümleleri tanır, ana dilinize bir çeviri gösterir, size hitap edildiğinde ise görüşme dilinde hazır bir yanıtı çevirisiyle birlikte sunar. Bir yanıta tıklamak onu kopyalar. «Yalnızca yanıt gerektiğinde» modu sadece yanıtlamanız gereken cümleleri gösterir.
- **Screenshot** (`2` / `Ctrl` + `Alt` + `2`). Ekran görüntüsü modele gider: görevi çözme, sınav sorusunu yanıtlama, kodu inceleme.
- **Watch** (`4` / `Ctrl` + `Alt` + `4`). Ekranı izler ve üzerinde yeni bir soru veya görev belirdiğinde yanıt verir. 10 dakika sonra kendiliğinden kapanır.
- **Sohbet**. Sıradan sorular. Başa yazılan bir rakam komutu seçer: `1` Quick (kısa, hızlı model), `3` Answer (son duyulan soruya, görüşmeyi dikkate alan tek bir yanıt), `5` Translate.
- Model görüşmenin son cümlelerini görür, bu yüzden sohbette «son sorularına nasıl yanıt vermeliyim?» diye sorabilirsiniz.
- **Bilgi tabanı**. Sık sorulan sorulara hazır yanıtlar içeren kendi `.txt` ve `.md` dosyalarınız. Uygun yanıt bilgisayarda, internetsiz bulunur ve model henüz yanıtlarken anında gösterilir.

## Kurulum

Hazır dosyalar `dist` klasöründedir:

- `Polymath-Setup-<sürüm>.exe` - kurulum programı, Windows diline uyar ve 22 dili destekler: klasörü seçebilirsiniz, yönetici hakları gerekmez, masaüstünde ve Başlat menüsünde kısayollar oluşur, program kurulumdan sonra başlar;

Windows SmartScreen bilinmeyen bir yayıncı uyarısı verebilir (dosya imzalı değildir). «Daha fazla bilgi» ve ardından «Yine de çalıştır» seçeneğine tıklayın.

Gereksinimler: Windows 10 sürüm 2004 (Mayıs 2020) veya daha yenisi, Windows 11. Daha eski sistemlerde ekran yakalamadan gizleme çalışmaz.

## İlk başlatma

1. Ayarları açın (çubuktaki dişli).
2. Bir model sağlayıcısı seçin, API anahtarını yapıştırın ve «Anahtarı kaydet» düğmesine tıklayın. «Anahtar al» bağlantısı sağlayıcının sayfasını açar.
3. «Bağlantıyı test et» düğmesine tıklayın. Kullanılabilir modellerin listesi görünür, bir modele tıklamak onu alana yazar.
4. Ana dilinizi belirtin. «Bilgi tabanı» bölümünde «Hakkınızda» alanına kendinizi kısaca anlatın (iş, deneyim). Model bunu yanıtlarında kullanır.
5. «Kaydet» düğmesine tıklayın (veya Ctrl+S).

### Sağlayıcılar

| Sağlayıcı                    | Varsayılan model         | Görüntü (Screenshot/Watch)  | Doğrudan ses   |
| ---------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini                | gemini-flash-lite-latest | evet                    | evet           |
| OpenAI                       | gpt-5-mini               | evet                    | hayır          |
| Anthropic Claude             | claude-sonnet-5-5        | evet                    | hayır          |
| OpenRouter                   | openrouter/auto          | evet                    | hayır          |
| Groq                         | openai/gpt-oss-120b      | hayır                   | hayır          |
| Mistral                      | mistral-medium-latest    | evet                    | hayır          |
| Ollama (yerel)               | llama3.2                 | hayır                   | hayır          |
| Özel (OpenAI uyumlu)         | herhangi biri            | modele bağlı            | hayır          |

Sağlayıcılar modellerin adını değiştirir. Bir model bulunamazsa «Bağlantıyı test et» düğmesine tıklayın ve listeden birini seçin.

«Hızlı model» Quick ve Translate komutlarında kullanılır. Boş bırakılabilir, o zaman ana model kullanılır.

Bir model 503 (aşırı yüklü) veya 429 (kota yok) yanıtı verdiğinde program çiftteki diğer modele hemen sorar.

### Yedek model

Ayarlardaki «Yedek model» bölümü: yukarıdaki iki model de 503 veya 429 yanıtı verdiğinde programın sorduğu başka bir sağlayıcı. Örneğin Anthropic Claude (varsayılan `claude-haiku-5-5`, hızlı bir model). Yedek anahtar ayrı saklanır. Anahtar yoksa «Model» bölümündeki aynı sağlayıcının anahtarı kullanılır. Yedek model, gönderileni okuyamadığı durumlarda atlanır: ekrandan bir görüntü (Screenshot/Watch) veya ses.

## Konuşma tanıma (Listen için)

Ayarlardaki «Konuşma tanıma» dört motor sunar:

1. **Model üzerinden** (varsayılan). Cümle doğrudan sohbet modeline gider. Aynı anahtarla Google Gemini ile çalışır.
2. **Bulut Whisper API**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, hızlı ve ucuz) veya OpenAI uyumlu kendi sunucunuz. Tanıma anahtarı model anahtarından ayrı saklanır.
3. **Yerel (whisper.cpp)**. Ses bilgisayardan asla çıkmaz. Tek komutla kurulur:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

Kurulu programda betik `<program klasörü>\resources\scripts` içindedir. Seçenekler: `-Model tiny|base|small|medium|large-v3-turbo` (varsayılan small, 466 MB) ve NVIDIA ekran kartları için `-Cuda`. Dosyalar `%APPDATA%\Polymath\whisper` içine gider. Sonra «Yerel» seçeneğini seçin ve «Tanımayı test et» düğmesine tıklayın.

4. **Yerel (NVIDIA Parakeet)**. Yine bu bilgisayarda, işlemcide whisper.cpp'den hızlı ve genellikle daha doğru. `parakeet-tdt-0.6b-v3` modeli 25 Avrupa dilini bilir (İngilizce, Rusça, Ukraynaca, Almanca, Fransızca, İspanyolca ve diğerleri), ancak Türkçe ve Çince'yi bilmez. [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) üzerinden çalışır. Ayarlardaki «Parakeet'i indir» düğmesi her şeyi yerine koyar, ya da tek komut:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

Toplam yaklaşık 520 MB. `-Model v2` seçeneği yalnızca İngilizce modeli alır, İngilizcede biraz daha doğrudur. Dosyalar `%APPDATA%\Polymath\parakeet` içine gider. Sonra «Yerel (NVIDIA Parakeet)» seçeneğini seçin ve «Tanımayı test et» düğmesine tıklayın. Bir moladan sonraki ilk cümle model yüklenirken 7-10 sn bekler, sonrakiler bir saniyenin altında sürer. 10 dakika konuşma olmazsa sunucu durur ve belleği boşaltır. Her iki indirme (program ve model) GitHub’ın yayımladığı SHA-256 ile denetlenir. Eşleşmeyen dosya silinir ve hiçbir şey kurulmaz. Yayımlanmış özet yoksa kurulum da yoktur.

Yeni bir bilgisayardaki ilk başlatmada çubuk sesin nasıl tanınacağını bir kez sorar: Gemini üzerinden (indirilecek bir şey yok) veya bu bilgisayarda Parakeet ile (uygulama yaklaşık 520 MB indirir, ilerleme ve iptal düğmesiyle). Yanıt sonradan ayarlardan değiştirilebilir.

«Tanımayı test et» düğmesi dört motorun hepsi için çalışır.

## Nasıl kullanılır

| Eylem                              | Kısayol                        |
| ---------------------------------- | ------------------------------ |
| Çubuğu göster / gizle              | `Ctrl` + `Alt` + `P`           |
| Hızlı yanıt (kısa, hızlı model) | `Ctrl` + `Alt` + `1` |
| Ekrandaki görevi çöz               | `Ctrl` + `Alt` + `2`           |
| Az önce duyulan soruya yanıt | `Ctrl` + `Alt` + `3` |
| Ekranı izle (açık/kapalı)          | `Ctrl` + `Alt` + `4`           |
| Çevir | `Ctrl` + `Alt` + `5` |
| Görüşmeyi dinle (açık/kapalı)      | `Ctrl` + `Alt` + `7`           |
| Çubuğun içinden tıkla (açık/kapalı)| `Ctrl` + `Alt` + `T`           |
| Gönder                             | `Enter`                        |
| Yeni satır                         | `Shift` + `Enter`              |
| Yanıtı durdur                      | `Ctrl` + `.` veya `■` düğmesi  |
| Yeni görüşme                       | `Ctrl` + `N` veya `+` düğmesi  |
| Önceki istek                       | boş alanda `↑` / `↓`           |
| Çubuğu gizle                       | `Esc`                          |

### Kısa ve uzun komutlar

Kısa komutlar çubuğun içinde, uzun olanlar (`Ctrl` + `Alt` ile) her pencereden çalışır. Boş alana yazılan rakam bir komut seçer, `1 metniniz` de çalışır.

| İşlem | Kısa (çubukta) | Uzun (her pencereden) |
| --- | --- | --- |
| Hızlı yanıt (kısa, hızlı model) | `1` | `Ctrl` + `Alt` + `1` |
| Ekrandaki görevi çöz | `2` | `Ctrl` + `Alt` + `2` |
| Az önce duyulan soruya yanıt | `3` | `Ctrl` + `Alt` + `3` |
| Ekranı izle (açık/kapalı) | `4` | `Ctrl` + `Alt` + `4` |
| Çevir | `5` | `Ctrl` + `Alt` + `5` |
| Görüşmeyi dinle (açık/kapalı) | `7` | `Ctrl` + `Alt` + `7` |
| Çubuğu göster / gizle | `Esc` | `Ctrl` + `Alt` + `P` |
| Çubuğun içinden tıkla (açık/kapalı) | - | `Ctrl` + `Alt` + `T` |
| Ayarlar | `Ctrl` + `,` | `Ctrl` + `,` |
| Yeni sohbet | `Ctrl` + `N` | - |
| Yanıtı durdur | `Ctrl` + `.` | - |
| Tüm kısayolları göster | `F1` | - |

**Çubuk gizli mi?** `Ctrl` + `Alt` + `P` tuşlarına (veya ayarlarda seçtiğiniz kısayola) basın ya da Polymath’i yeniden başlatın (Başlat menüsündeki kısayol), çubuk geri gelir. Sistem tepsisi simgesi varsayılan olarak kapalıdır. Çubuktaki `?` düğmesi (ayarların yanında, veya `F1`) tüm komutları ve kısayolları gösterir.

**Önemli:** kısa komutlar yalnızca giriş alanı etkinken çalışır, tıklama geçirme modunda çalışmaz. Uzun komutlar (`Ctrl` + `Alt` ile) her zaman çalışır.

Kısayollar ayarlarda değiştirilir: alana tıklayın ve tuş birleşimine basın. Başka bir program onu zaten kullanıyorsa çubuk bunu bildirir.

Çubuğu başlığından sürükleyin, konumu hatırlanır. Genişlik, saydamlık ve yazı boyutu ayarlanabilir.

### Görünüm ve fare

Ayarlardaki «Arayüz» bölümü:

- **Tema** - koyu (grafit, varsayılan) veya açık (fildişi);
- **Çubuk opaklığı** - metniyle birlikte tüm çubuk (%30-100);
- **Arka plan opaklığı** - yalnızca çubuğun arka planı, metin net kalır (%20-100);
- **Çubuğun içinden tıkla** - tıklamalar yardımcı çubuğun içinden geçip altındaki pencereye ulaşır. Çubuk fareyle taşınamaz ve tıklanamaz, klavye ve kısayollar çalışmaya devam eder. `Ctrl` + `Alt` + `T` ile açılıp kapanır, çubuk başlığında o sırada «içinden tıklama» işareti görünür. Ayarlar penceresi her zaman normal bir penceredir;
- **Düğmelere üzerinde bekleyerek bas** - imleci çubuktaki bir düğmenin üzerinde tutun (varsayılan 3 saniye, 1,5 ile 5 arası) ve düğme kendiliğinden basılır. Düğmenin altında bir şerit dolar. İçinden tıklama modunda da çalışır.

Listen tüm sistemin sesini yakalar. Kulaklık kullanın: böylece yalnızca karşıdaki kişi kaydedilir, kendi sesiniz değil.

## Kendi komutlarınız

Rakamlı komutlar `%APPDATA%\Polymath\commands.json` dosyasındadır (ayarlardaki «commands.json'u aç» düğmesi). Dosya her çağrıda yeniden okunur, yeniden başlatmak gerekmez. Örnek:

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Alanlar: `name`, `instructions` (zorunlu), `model` (`main` veya `small`), `screen: true` (ekran görüntüsü ekle), `watch: true` (ekranı izle), `listen: true` (Listen'ı aç). Yer tutucular: `{native}` - dilinizdir, `{conversation_language}` - görüşme dilidir.

## Gizlemenin güvenilirliği

Pencereler `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)` ile oluşturulur. Bu bir Windows mekanizmasıdır: ekran görüntüsü o yerde pencerenin altındakini gösterir. Zoom, Teams, tarayıcıda Google Meet, Discord, OBS, Ekran Alıntısı Aracı, PrintScreen ve Xbox Game Bar buna uyar.

Ayrıca:

- görev çubuğunda düğme ve Alt+Tab'de giriş yoktur;
- tepsi simgesi varsayılan olarak kapalıdır (tüm ekran paylaşıldığında tepsi görünür);
- sistemin açılır pencereleri yoktur: ipuçları, listeler ve menüler çubuğun içine çizilir, bağlam menüsü kapalıdır.

Sınırlar:

- Gizleme, monitöre doğrultulmuş bir kameradan veya donanımsal HDMI yakalamadan korumaz.
- Bir programın **penceresini** paylaşıyorsanız (tüm ekranı değil) ve çubuk onun üzerindeyse, karşı taraf çubuğun altındakini görür. Bu beklenen davranıştır.
- Windows 10 sürüm 2004'ten eski sürümler yakalamada çubuk yerine siyah bir dikdörtgen gösterir.
- Açılan bağlantılar ve dosyalar (commands.json, veri klasörü) sıradan programlarda açılır ve ekran paylaşılırken görünür.

Gizlemeyi kendi bilgisayarınızda doğrulayın:

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

Betik korumalı iki test penceresi ve bir normal pencere gösterir, ekranı iki yöntemle yakalar ve sonucu yazdırır. `RESULT: Polymath windows are hidden from screen capture` satırı her şeyin çalıştığı anlamına gelir.

## Bilgi tabanı

Ayarlardaki «Bilgi tabanı» bölümü:

- **Hakkınızda** - sizin hakkınızda genel bilgi. Model bunu her yanıtta kullanır.
- **Dosyalar** - «Dosya ekle» düğmesi veya `.txt` ve `.md` dosyalarını bölümün üzerine bırakın. Dosyalar `%APPDATA%\Polymath\knowledge` içine kopyalanır («Klasörü aç» düğmesi). Orada düzenleyebilirsiniz, program değişiklikleri kendisi alır. Aynı adlı dosya değiştirilir, en fazla 2 MB, UTF-8, UTF-16 veya Windows-1251.
- **Yanıtlarda bilgi tabanını kullan** - tabanda bir dosya olunca açılır.
- **Tabandaki eşleşmeyi model yanıtlamadan önce hemen göster** - aynı şekilde.

Nasıl çalışır. Sohbetteki bir soru için ve Listen'daki karşıdaki kişinin her cümlesi için program önce dosyalarınızda bir yanıt arar, internetsiz ve modelsiz. Eşleşme hemen modelin yanıtının üstünde mavi bir «Bilgi tabanından» bloğu olarak belirir, yanında bir «Kopyala» düğmesi vardır. Aynı anda model bu verileri alır (taban küçükse tamamını, değilse eşleşen kısımları) ve bunlara dayanarak yanıt verir. Arama kelimelerin farklı biçimlerini anlar. Yerel arama başka bir dildeki soruyu bulamaz, ancak model yine de tabandan yanıt verir.

Dosyaları yazmanın üç yolundan biri:

```markdown
# What salary do you expect?
From 5,000 USD net, open to discussion.

# Why are you leaving your current job?
I want more architecture work.
```

```text
Q: What is your notice period?
A: Two weeks.
```

Ya da sadece boş satırla ayrılmış paragraflar: bir paragrafın kısa ilk satırı onun konusudur.

## Geçmiş ve dışa aktarma

Ayarlardaki «Geçmiş» bölümü:

- **Geçmişi diske kaydet**. Varsayılan olarak kapalıdır: geçmiş o zaman program kapanana kadar yalnızca bellekte yaşar. Açıkken her soru ve yanıt `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl` dosyasına eklenir, her satır Windows DPAPI ile şifrelenir (yalnızca Windows hesabınız okuyabilir).
- **Geçmişteki ad**. Dışa aktarmalarda sorularınızı imzalar. Boş olması Windows kullanıcı adı demektir.
- **Saklama, gün**. Daha eski günler başlangıçta silinir. 0 her şeyi saklar.
- **Dışa aktar**: bu oturum, bugün, 7 gün, 30 gün veya tüm zaman. «.txt olarak dışa aktar» `Documents\Polymath` içine bir dosya kaydeder, «Metin olarak kopyala» aynı metni panoya koyar.
- **Geçmişi temizle** geçmiş dosyalarını ve bu oturumun kayıtlarını siler (düğmeye iki kez basın).

Neler kaydedilir:

- sohbet: Q - sorunuz (komut ve ekran görüntüsü işaretiyle), A - modelin yanıtı;
- Listen: Q - karşıdaki kişinin cümlesi ve çevirisi, A - size önerilen yanıt ve çevirisi (yanıt gerektiğinde);
- Watch: ekrandaki görevlere yanıtlar, boş çalıştırmalar kaydedilmez.

Dışa aktarma dosyası şifrelenmez. «Dosyayı göster» düğmesiyle açılan Gezgin ve Not Defteri ekran paylaşılırken görünür.

## Gizlilik

- API anahtarları Windows tarafından şifrelenmiş olarak (Electron safeStorage üzerinden DPAPI) `%APPDATA%\Polymath\settings.json` içinde saklanır.
- Varsayılan olarak geçmiş yalnızca bellektedir ve program kapanınca kaybolur. Diske kaydetme ayarlardan açılır, geçmiş dosyaları DPAPI ile şifrelenir.
- Bilgi tabanı dosyaları `%APPDATA%\Polymath\knowledge` içinde şifrelenmeden saklanır, arama bilgisayarda yapılır. Modele yalnızca bir soruyla gider: taban küçükse tamamı, değilse eşleşen kısımlar.
- Ses ve ekran görüntüleri yalnızca seçilen sağlayıcıya (veya yedeğe) ve yalnızca Listen, Screenshot veya Watch açıkken gider. Yerel whisper.cpp veya Parakeet ile ses bilgisayardan asla çıkmaz.
- Hata günlüğü: `%APPDATA%\Polymath\logs\app.log` (görüşme metni olmadan).

## Arka planda çalışma

«Windows oturumu açılınca başlat» kutusu Polymath'i gizli başlatır. Çubuğu Ctrl+Alt+P ile çağırın. Elle: `Polymath.exe --background`.

## Güncellemeler

Kurulu Polymath (`Polymath-Setup` ile kurulan), açıldıktan birkaç saniye sonra yeni sürüm arar. Sizin onayınız olmadan hiçbir şey indirilmez: çubukta „Polymath X kullanılabilir“ iletisi „Güncelle“ ve „Sonra“ düğmeleriyle görünür, indirme bitince „Yeniden başlat ve güncelle“ çıkar. Polymath kapanır, eski sürümün üzerine kurulur ve yeniden başlar, ayarlar, anahtarlar ve geçmiş korunur. Tepsi simgesi açıksa menüsünde „Check for updates“ vardır. Kaynak klasöründen çalıştırılan kopya ve taşınabilir kopya kendini güncellemez.

İndirilen dosya, sürümün `latest.yml` dosyasındaki SHA-512 ile denetlenir. Bu özeti olmayan sürüm reddedilir, eşleşmeyen dosya kurulmaz. Her derleme `latest.yml` içinde doğru özetin bulunduğunu denetler. Kurulum programı henüz imzalı değildir, bu yüzden Windows SmartScreen yine de uyarabilir.

## Geliştiriciler için

Node.js 20 veya üstü gerekir.

```powershell
npm install
```

```powershell
npm start
```

```powershell
npm test
```

```powershell
npm run dist
```

- `npm test` - birim testleri (cümle algılayıcı, WAV, yanıt ayrıştırma, SSE, komutlar, ayarlar, model istemcisi, geçmiş).
- `npm run dist` - `dist` içinde kurulum programı, ardından `latest.yml` içinde doğru SHA-512 olduğunun denetimi.
- `python scripts/make-installer-art.py` - kurulum programının görsellerini (`build/`: yan görsel, başlık, simge) `assets/icon.png` dosyasından yeniden çizer. Pillow'lu Python gerekir.
- `npm run capture-test` - yerleşik gizleme denetimi (sonuç JSON olarak).
- `POLYMATH_VISIBLE=1` değişkeni geliştirme modunda gizlemeyi kapatır, arayüzün ekran görüntülerini almak için. Derlenmiş programda hiçbir etkisi yoktur.

Yapı:

- `src/main` - ana süreç: pencereler, kısayollar, model, konuşma tanıma, Listen, Watch;
- `src/renderer` - çubuk ve ayarlar penceresi, sistem sesinin yakalanması;
- `src/shared` - ortak kod: cümle algılayıcı, WAV, metin ayrıştırma, SSE, arayüz çevirileri;
- `scripts` - whisper.cpp ve Parakeet kurulumu ile gizleme denetimi;
- `tests` - testler.
