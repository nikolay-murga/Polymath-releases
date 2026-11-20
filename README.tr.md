# Windows için Polymath

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

Görüşmeler ve toplantılar için küçük bir yardımcı çubuk. Karşınızdaki kişiyi dinler ve konuşmasını sizin dilinize çevirir, konuşmanın dilinde bir yanıt önerir, ekrandaki bir görevi çözer ve sohbette her soruyu yanıtlar.

**Çubuğu yalnızca siz görürsünüz.** Zoom, Teams, Meet, Discord veya OBS'de ekranınızı paylaştığınızda, ayrıca ekran görüntülerinde ve ekran kayıtlarında görünmez.

## Özellikler

- **Dinle**. Bilgisayarın sesini dinler (bir aramada karşı tarafın sesi), cümleleri tanır, ana dilinize çeviriyi gösterir ve size hitap edildiğinde, konuşmanın dilinde hazır bir yanıtı çevirisiyle birlikte gösterir. Kopyalamak için bir yanıta tıklayın. «Yalnızca yanıt gerektiğinde» modu yalnızca yanıt vermeniz gereken satırları gösterir.
- **Ekran**. Model'e bir ekran görüntüsü gönderilir: bir görevi çözme, bir test sorusunu yanıtlama, kod inceleme.
- **İzle**. Ekranı izler ve ekranda yeni bir soru ya da görev belirdiğinde yanıt verir. 10 dakika sonra kendiliğinden kapanır.
- **Sohbet**. Olağan sorular. Başta bir rakam bir komutu seçer: `1` Hızlı (kısa, hızlı model), `3` Yanıt (son duyulan soruya, konuşmayı dikkate alarak yanıt), `5` Çeviri.
- Model konuşmanın son cümlelerini görür, bu yüzden sohbette şunu sorabilirsiniz: «son sorularına nasıl yanıt vereyim?».
- **Bilgi tabanı**. Sık sorulan sorular için hazır yanıtlar içeren kendi `.txt` ve `.md` dosyalarınız. Uygun yanıt bilgisayarda, internet olmadan bulunur ve model hâlâ yanıt yazarken hemen gösterilir.
- **Kendi komutlarınız**. Kendi talimatlarınız, modeliniz ve ekran ya da ses ayarlarınızla rakamlı komutlar ekleyin.
- **Geçmiş ve dışa aktarma**. Görüşmelerin isteğe bağlı, şifreli olarak kaydedilmesi ve bir metin dosyasına aktarılması.

## Kurulum

Her sürümde iki hazır dosya yayımlanır:

- `Polymath-Setup-<sürüm>.exe` - Windows dilinize göre açılan kurulum programı, 22 dil desteklenir. Klasörü siz seçersiniz, yönetici hakları gerekmez, kısayollar masaüstüne ve Başlat menüsüne eklenir ve kurulumdan sonra program açılır.

Dosya henüz imzalanmadığı için Windows SmartScreen bilinmeyen bir yayımcı konusunda uyarabilir. «Ek bilgi» ve ardından «Yine de çalıştır» seçeneğine tıklayın.

Gereksinimler: Windows 10 sürüm 2004 (Mayıs 2020) veya daha yeni, ya da Windows 11. Daha eski sistemlerde ekran paylaşımından gizlenme çalışmaz.

Güncellemeler: Kurulu bir kopya, başladıktan birkaç saniye sonra bu sayfada yeni sürüm olup olmadığını kontrol eder. Daha yeni bir sürüm çıktığında program bir kart gösterir ve güncellemeyi yalnızca sizin onayınızla indirir. Güncelleme aynı klasöre kurulur ve program yeniden başlar.

## İlk başlatma

1. Ayarları açın (çubuktaki dişli simgesi).
2. Bir model sağlayıcısı seçin, API anahtarını yapıştırın ve «Anahtarı kaydet» düğmesine tıklayın. «Anahtar al» bağlantısı sağlayıcının sayfasını açar.
3. «Bağlantıyı test et» düğmesine tıklayın. Kullanılabilir modellerin listesi görünür, bir modele tıklamak onu alana yerleştirir.
4. Ana dilinizi seçin. «Bilgi tabanı» bölümünde «Hakkınızda» alanına kendinizi kısaca yazın (meslek, deneyim). Model bunu yanıtlarında kullanır.
5. «Kaydet» düğmesine tıklayın (ya da Ctrl+S tuşlarına basın).

### Sağlayıcılar

| Sağlayıcı                        | Varsayılan model         | Resimler (Ekran/İzle) | Ses doğrudan |
| -------------------------------- | ------------------------ | --------------------- | ------------ |
| Google Gemini                    | gemini-flash-lite-latest | evet                  | evet         |
| OpenAI                           | gpt-5-mini               | evet                  | hayır        |
| Anthropic Claude                 | claude-sonnet-5-5        | evet                  | hayır        |
| OpenRouter                       | openrouter/auto          | evet                  | hayır        |
| Groq                             | openai/gpt-oss-120b      | hayır                 | hayır        |
| Mistral                          | mistral-medium-latest    | evet                  | hayır        |
| Ollama (yerel)                   | llama3.2                 | hayır                 | hayır        |
| Özel (OpenAI uyumlu)             | istediğiniz              | modele bağlı          | hayır        |

Sağlayıcılar modellerinin adlarını değiştirir. Bir model bulunamazsa «Bağlantıyı test et» düğmesine tıklayın ve listeden birini seçin.

«Hızlı model», «Hızlı» ve «Çeviri» komutları tarafından kullanılır. Boş bırakılabilir, bu durumda ana model kullanılır.

Bir model 503 (aşırı yüklü) veya 429 (kota doldu) yanıtı verdiğinde program hemen çiftteki diğer modele sorar.

### Yedek model

Ayarlardaki «Yedek model» bölümü, yukarıdaki iki model 503 veya 429 yanıtı verdiğinde programın sorduğu başka bir sağlayıcıyı belirler. Örneğin Anthropic Claude (varsayılan olarak `claude-haiku-5-5`, hızlı bir model). Yedek anahtar ayrı saklanır. Yoksa «Model» bölümündeki aynı sağlayıcının anahtarı kullanılır. Yedek, gönderilen içeriği okuyamadığında atlanır: bir ekran resmi (Ekran/İzle) ya da ses gibi.

## Konuşma tanıma (Dinle için)

«Konuşma tanıma» ayarlarında dört seçenek bulunur:

1. **Model üzerinden** (varsayılan). Cümle doğrudan sohbet modeline gider. Google Gemini ile, aynı anahtarla çalışır.
2. **Bulut Whisper API**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, hızlı ve ucuz) veya OpenAI uyumlu kendi sunucunuz. Tanıma anahtarı model anahtarından ayrı saklanır.
3. **Yerel (whisper.cpp)**. Ses hiçbir zaman bilgisayardan çıkmaz. Tek bir komutla kurulur, dosyalar `%APPDATA%\Polymath\whisper` klasörüne gider. Ardından «Yerel» seçin ve «Tanımayı test et» düğmesine tıklayın. Varsayılan olarak küçük model kullanılır (466 MB). Diğer boyutlar ve NVIDIA ekran kartlarında hızlandırma, kurulum betiğinin seçenekleri olarak mevcuttur.
4. **Yerel (NVIDIA Parakeet)**. Yine bu bilgisayarda, işlemcide whisper.cpp'den hızlı ve genellikle daha doğru. Model 25 Avrupa dilini bilir (İngilizce, Rusça, Ukraynaca, Almanca, Fransızca, İspanyolca ve diğerleri), ancak Türkçe ve Çinceyi bilmez. Ayarlardaki «Parakeet'i indir» düğmesi modeli yerleştirir. Toplamda yaklaşık 520 MB. Ardından «Yerel (NVIDIA Parakeet)» seçin ve «Tanımayı test et» düğmesine tıklayın. Bir duraklamadan sonraki ilk cümle, model yüklenirken 7-10 saniye bekler, sonrakiler bir saniyeden kısa sürer. 10 dakika konuşma olmazsa sunucu durur ve belleği serbest bırakır.

Yeni bir bilgisayarda ilk başlatmada çubuk konuşmayı nasıl tanıyacağını bir kez sorar: Gemini üzerinden (indirilecek bir şey yok) ya da bu bilgisayarda Parakeet ile (program yaklaşık 520 MB indirir, ilerleme göstergesi ve iptal düğmesiyle). Yanıt daha sonra ayarlardan değiştirilebilir.

«Tanımayı test et» düğmesi dört seçeneğin hepsinde çalışır.

## Nasıl kullanılır

| Eylem                              | Kısayol                        |
| ---------------------------------- | ------------------------------ |
| Çubuğu göster / gizle              | `Ctrl` + `Alt` + `P`           |
| Ekrandaki görevi çöz               | `Ctrl` + `Alt` + `2`           |
| Ekranı izle (açık/kapalı)          | `Ctrl` + `Alt` + `4`           |
| Görüşmeyi dinle (açık/kapalı)      | `Ctrl` + `Alt` + `7`           |
| Çubuğun içinden tıklama (açık/kapalı) | `Ctrl` + `Alt` + `T`        |
| Gönder                             | `Enter`                        |
| Yeni satır                         | `Shift` + `Enter`              |
| Yanıtı durdur                      | `Ctrl` + `.` veya `■` düğmesi  |
| Yeni sohbet                        | `Ctrl` + `N` veya `+` düğmesi  |
| Önceki istek                       | Boş alanda `↑` / `↓`           |
| Çubuğu gizle                       | `Esc`                          |

Kısayollar ayarlarda değiştirilir: alana tıklayın ve kısayola basın. Kısayolu başka bir program zaten kullanıyorsa çubuk bunu bildirir.

Çubuğu başlığından sürükleyerek taşıyabilirsiniz, yeri hatırlanır. Genişlik, saydamlık ve yazı boyutu ayarlanabilir.

### Görünüm ve fare

Ayarlardaki «Arayüz» bölümü:

- **Tema**: koyu (grafit, varsayılan) veya açık (fildişi).
- **Çubuğun saydamlığı**: metinle birlikte tüm çubuk (%30-100).
- **Arka plan saydamlığı**: yalnızca çubuğun arka planı, metin keskin kalır (%20-100).
- **Çubuğun içinden tıklama**: tıklamalar yardımcı çubuğun içinden geçip altındaki pencereye ulaşır. Bu modda çubuk fareyle taşınamaz ve tıklanamaz, ancak klavye ve kısayollar çalışmaya devam eder. `Ctrl` + `Alt` + `T` ile açılıp kapatılır ve bu modda çubuğun başlığında «içinden tıklama» işareti görünür. Ayarlar penceresi her zaman normal bir pencere olarak kalır.
- **Düğmeleri üzerine gelerek bas**: imleci çubuktaki bir düğmenin üzerinde tutun (varsayılan 3 saniye, 1,5 ile 5 arası seçilebilir) ve düğme kendiliğinden basılır. Düğmenin altında bir şerit dolar. İçinden tıklama modunda da çalışır.

«Dinle» tüm sistemin sesini yakalar. Kulaklık kullanın: böylece yalnızca karşı taraf kaydedilir, kendi sesiniz kaydedilmez.

## Kendi komutlarınız

Rakamlı komutlar `%APPDATA%\Polymath\commands.json` dosyasında tutulur (ayarlardaki «commands.json'u aç» düğmesi). Dosya her çağrıda yeniden okunur, yeniden başlatmaya gerek yoktur. Örnek:

```json
{
  "1": {
    "name": "Mülakat",
    "instructions": "Bir iş mülakatında kıdemli bir Java geliştiricisi gibi yanıt ver. {conversation_language} dilinde yanıt ver, ardından {native} diline kısa bir çeviri ekle.",
    "model": "main"
  }
}
```

Alanlar: `name`, `instructions` (zorunlu), `model` (`main` veya `small`), `screen: true` (ekran görüntüsü ekler), `watch: true` (ekranı izler), `listen: true` (Dinle'yi açar). Yer tutucular: `{native}` sizin dilinizdir, `{conversation_language}` ise konuşmanın dilidir.

## Ekran paylaşımından gizlenme

Pencereler, onları yakalamanın dışında bırakan Windows mekanizmasıyla oluşturulur (`WDA_EXCLUDEFROMCAPTURE`). Ekran yakalandığında çubuğun yerine altındaki içerik görünür. Zoom, Teams, tarayıcıdaki Google Meet, Discord, OBS, Ekran Alıntısı, PrintScreen ve Xbox Game Bar bu mekanizmaya uyar.

Ayrıca:

- görev çubuğunda düğme yoktur ve Alt+Tab listesinde görünmez;
- bildirim alanı simgesi varsayılan olarak kapalıdır (tüm ekran paylaşıldığında bildirim alanı görünür);
- sistem pencereleri açılmaz: ipuçları, listeler ve menüler çubuğun içinde çizilir, bağlam menüsü kapalıdır.

Sınırlar:

- Gizlenme, monitöre doğrultulmuş bir kameraya ya da donanımsal HDMI yakalamaya karşı koruma sağlamaz.
- Bir programın tüm ekranını değil de yalnızca **penceresini** paylaşıyorsanız ve çubuk onun üstündeyse, karşı taraf çubuğun altındakini görür. Bu beklenen bir durumdur.
- Windows 10'un 2004 sürümünden eski sistemlerde yakalamada çubuk yerine siyah bir dikdörtgen görünür.
- Açılan bağlantılar ve dosyalar (commands.json, veri klasörü) sıradan programlarda açılır ve ekran paylaşıldığında görünür.

## Bilgi tabanı

Ayarlardaki «Bilgi tabanı» bölümü:

- **Hakkınızda**: sizinle ilgili genel bilgiler. Model bunu her yanıtta kullanır.
- **Dosyalar**: «Dosya ekle» düğmesi ya da bölüme `.txt` ve `.md` dosyalarını sürüklemek. Dosyalar `%APPDATA%\Polymath\knowledge` klasörüne kopyalanır («Klasörü aç» düğmesi). Orada düzenleyebilirsiniz, program değişiklikleri kendisi algılar. Aynı adlı dosya yenisiyle değiştirilir. Sınır dosya başına 2 MB, kodlama UTF-8, UTF-16 veya Windows-1251.
- **Yanıtlarda bilgi tabanını kullan**: tabanda bir dosya olduğunda açılır.
- **Model yanıt vermeden önce tabandan eşleşmeyi hemen göster**: aynısı.

Nasıl çalışır. Sohbetteki bir soru ve «Dinle» modunda karşı tarafın her cümlesi için program önce yanıtı dosyalarınızda arar, internet ve model kullanmadan. Eşleşme, modelin yanıtının üstünde mavi bir «Bilgi tabanından» bloğu olarak hemen görünür ve yanında bir «Kopyala» düğmesi bulunur. Aynı anda model bu veriyi alır (taban küçükse tamamı, değilse bulunan bölümler) ve ona dayanarak yanıt verir. Arama kelimelerin farklı biçimlerini anlar. Yerel arama başka bir dilde yazılmış bir soruyu bulamaz, ama model yine de tabana göre yanıt verir.

Dosyaları yazmanın üç yolu:

```markdown
# Ne kadar maaş bekliyorsunuz?
Net 5.000 USD'den başlayarak, pazarlığa açığım.

# Mevcut işinizden neden ayrılıyorsunuz?
Mimari işlerde daha fazla çalışmak istiyorum.
```

```text
Q: İhbar süreniz nedir?
A: İki hafta.
```

Ya da boş satırla ayrılmış paragraflar. Bir paragrafın kısa ilk satırı konusudur.

## Geçmiş ve dışa aktarma

Ayarlardaki «Geçmiş» bölümü:

- **Geçmişi diske kaydet**. Varsayılan olarak kapalıdır: geçmiş program kapanana kadar yalnızca bellekte tutulur. Açıkken her soru ve yanıt `%APPDATA%\Polymath\history` içindeki günlük dosyaya eklenir ve her satır Windows DPAPI ile şifrelenir, bu yüzden yalnızca Windows hesabınız okuyabilir.
- **Geçmişteki ad**. Dışa aktarmalarda sorularınızın altına yazılacak addır. Boş bırakılırsa Windows kullanıcı adı kullanılır.
- **Saklama süresi, gün**. Eski günler başlangıçta silinir. 0 her şeyi saklar.
- **Dışa aktar**: bu oturum, bugün, 7 gün, 30 gün veya tüm zamanlar. «.txt olarak dışa aktar» dosyayı `Belgeler\Polymath` klasörüne kaydeder, «Metin olarak kopyala» aynı metni panoya koyar.
- **Geçmişi temizle** geçmiş dosyalarını ve bu oturumun kayıtlarını siler (düğmeye iki kez basmanız gerekir).

Neler kaydedilir:

- sohbet: soru (komut ve ekran görüntüsü işaretiyle) ve modelin yanıtı;
- Dinle: karşı tarafın cümlesi ve çevirisi, bir yanıt gerektiğinde önerilen yanıt ve çevirisi;
- İzle: ekrandaki görevlere verilen yanıtlar. Boş çalıştırmalar kaydedilmez.

Dışa aktarma dosyası şifrelenmez. «Dosyayı göster» düğmesiyle açılan Dosya Gezgini ve Not Defteri, ekran paylaşıldığında görünür.

## Gizlilik

- API anahtarları Windows tarafından şifreli olarak (DPAPI) `%APPDATA%\Polymath\settings.json` dosyasında saklanır.
- Varsayılan olarak geçmiş yalnızca bellektedir ve program kapandığında silinir. Diske kaydetme ayarlardan açılır ve geçmiş dosyaları DPAPI ile şifrelenir.
- Bilgi tabanı dosyaları `%APPDATA%\Polymath\knowledge` klasöründe şifrelenmeden saklanır ve bilgisayarda aranır. Modele yalnızca bir soruyla birlikte gider: taban küçükse tamamı, değilse eşleşen bölümler.
- Ses ve ekran görüntüleri yalnızca seçilen sağlayıcıya (veya yedek sağlayıcıya) gider ve yalnızca «Dinle», «Ekran» ya da «İzle» açıkken. Yerel whisper.cpp ya da Parakeet ile ses hiçbir zaman bilgisayardan çıkmaz.
- Hata günlüğü `%APPDATA%\Polymath\logs\app.log` dosyasındadır. Görüşme metni içermez.

## Arka planda çalıştırma

«Windows oturumu açılırken başlat» kutusu Polymath'i gizli olarak başlatır. Çubuğu `Ctrl` + `Alt` + `P` ile çağırın.

## Gereksinimler ve sınırlar

- Windows 10 sürüm 2004 veya daha yeni ya da Windows 11.
- Bulut modelleri için internet gerekir. Yerel konuşma tanıma kurulumdan sonra ağ olmadan çalışır.
- En az bir model sağlayıcısının anahtarı. Anahtarlar size aittir, ücreti sağlayıcı keser.
