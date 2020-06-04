# <center> Görüntü İşleme </center>

**Ayrık zaman işareti:** Gerçek ya da karmaşık sayıların oluşturduğu bir diziyi ifade etmektedir

**Nyquist:** Bulunan maksimum frekans bileşeni Nyquist frekansı olarak adlandırılır.

**Niceleme :** Sayısal işaret ve görüntü işleme alanlarında sürekli ya da büyük bir değerler kümesinin daha az sayıda ve ayrık değerlere eşlenmesine nicemleme veya "kuantalama" denir.

**İşaretler:**

- Sürelerine göre sonlu ve sonsuz süreli (uzunluklu) olmak üzere ikiye ayrılırlar. Sonsuz uzunluklu diziler sağ yanlı ve sol yanlı olmak üzere iki alt sınıfa ayrıştırılabilir.
- İşaretin kendini belli aralıklarla tekrarlayıp tekrarlamadığına bakılarak da **periyodik** ve **aperiyodik** (periyodik olmayan) diziler olarak iki sınıfa ayrılabilir.
- İşaret, zaman içerisinde istatistiksel özelliklerini (standart sapma, genlik dağılımı, ortalama v.b.) s**abit olarak koruyorsa durağan**, zaman içinde **değişikli gösteren parametreler sahipse durağan olmayan** işaret olarak adlandırılır.
- İşaretler **simetriklik özelliğine**bakılarak **gerçek** ve **karmaşık** değerli işaretler olmak üzere ikiye ayrılırlar.

**Frekans, Periyot, Dalgaboyu**

- **Frekans** İşaretin 1 saniyedeki tekrarlama (cycle-saykıl-
  döngü) sayısıdır. Birimi Hertz’dir (f=1/T)

- **Periyot** İşaretin bir saykılını tamamlama süresidir. Birimi saniyedir. Frekansın tersidir. (T=1/f)

- **Dalgaboyu**: Sinyalin bir döngüsündeki(saykıl) aldığı
  mesafesidir. Birimi metredir (λ=c/f)

**Frekans Bölgesi Kavramları**

- İşaretler genellikle çok frekanstan oluşur.
  - Tüm işaretler için temel dalga Sinüs işaretidir.
  - İşaretler Fourier analizi ile sinüs dalgası bileşenlerine ayrılabilir.
  - Peryodik şaretleri, temel frekansın tam katlarındaki sinüsoidal işaretlerden oluşurlar.

**Frekans Domeni**

- İşaretin frkenas spektrumunda işgal ettiği yere bant genişliği denir

**Süzgeçler:** Sayısal süzgeçler/filtreler yardımıyla giriş işareti (sayı dizisi) bir dizi hesapsal işlem veya algoritmalar ile bir çıkış dizisine dönüştürülür.

**Süzgeçler özelliklerine:** (doğrusallık, ötelemeyle değişmezlik) karakterize edilirler ve frekans cevaplarına göre sınıflandırılırlar (alçak ve yüksek geçiren, bant durduran ve geçiren süzgeçler gibi).

**Konvolüsyon (Katlama)**

- Bir ayrık zamanlı sistem bir giriş işaretini sabit kurallar kümesi veya
  işlemleriyle başka bir çıkış işaretine dönüştüren matematiksel bir
  operatör olarak tanımlanabilir.

# <center>SAYISAL GÖRÜNTÜ İŞLEMEYE GİRİŞ</center>

- Çeşitli algılayıcılar (kameralar, tarayıcılar, tıbbi ve uzaktan
  algılama cihazları gibi) tarafından oluşturulan,
- Görsel olarak iki boyutta ifade edilmekle beraber daha
  yüksek boyutta bileşenlere sahip olabilen dış dünya
  işaretleridir.

**Sayısal Görüntünün Oluşturulması**

- Gerçek dünyadan (analog) sayısal dünyaya geçiş veya diğer bir
  deyişle dış uzaydan 2 boyutlu uzaya (I(x,y)) geçiş, nesnelerin
  üzerine yansıyan ışığın, kamera gibi çeşitli sayısallaştırıcı
  algılayıcılar vasıtası ile algılanması şeklinde gerçekleştirilir.
- Burada dikkat edilmesi gereken husus gerçek dünyadan sayısal
  dünyaya geçişte kullanılan cihazın algılayıcı kalitesi ve ayarlarına
  göre bilgi kaybının yaşanacağıdır.
- Bu işlem ‘Örnekleme’ ve ‘Nicemleme’ adımlarını içerir:

**2 Boyutlu Örnekleme:** Görüntüden belirli uzamsal aralıklarda gerek x gerek y yönünde örnekler alınarak sayısallaştırılacak hale getirilmesidir.

**Nicemleme:** Görüntüden alınan örneklerin genliklerinin sadece belirli değerleri alacak şekilde düzenlenmesi işlemidir

**Piksel (Görüntü Elemanı):** Bir görüntünün en temel elemanı örneklenmiş olan uzamsal noktaların değerleridir ve görüntü elemanı (picture element) piksel (pixel) olarak adlandırılır.

**Uzamsal Çözünürlük:** Belirli bir bölgede alınan uzamsal örneklerin sayısı “uzamsal çözünürlüğü” belirler. Birimi ppi (piksel per inch), dpi (dot per inch) veya ppm (pixel per meter) olarak belirtilebilir

<center><image src="./image/uzamsal.jpg" width="300"></image></center>

**Nicemlemede Seçilen Bit Sayısına Göre**:

- Nicemlemede seçilen bit sayısı da piksellerin belirteceği
  - Genlik aralıklarının darlığı ile ters orantılı olduğu için
  - Görüntünün kalitesini belirlemede önemli bir parametredir.

**Görüntü Renk Biçimleri**:

- Analog dünyada renkler, 380-760 nm dalga boyuna sahip
  elektromanyetik dalgaların nesneler tarafından yansıtılıp, görme üzerine
  özelleşmiş bir organ olan göz tarafından algılanması ile insan beyninde
  oluşturulur
- Elektromanyetik renk spektrumunda kızılötesi ve mor ötesi (infrared ve
  ultraviyole) arasına denk düşen bant aralığı görünür ışık bölgesi olarak
  adlandırılır.
- Gözde bulunan koni ve çubuk tipindeki algılayıcılar vasıtasıyla bu bant
  aralığındaki renkler ayırt edilebilir.
- Renk kavramının algılanabilmesi için nesnelerden yansıyan ışığın
  parlaklık (brightness) ve renklilik (chrominance) bilgilerinin anlaşılması
  gerekmektedir.

<center><image src="./image/elektromanyetik.jpg" width="1000"></image></center>

- Bu tayfın üst sınırında yer alıp göremediğimiz ışınlara morötesi, bu tayfın alt sınırında yer alıp da göremediğimiz ışınlara kızılaltı ışınlar veya radyasyonlar denir.
- Üst ve alt sınırlar arasındaki gözle görülebilen tayf alanı içindeki tüm ışınımlar bir kaynaktan veya yansıdıkları yerden göze birlikte ulaşırlarsa beyaz renkli görünürler.
- İnsan gözünün algılayabildiği **yedi temel dalga boyu** **kırmızı, turuncu, sarı, yeşil, mavi, çivit ve mordur**

**Görüntü Renk Biçimleri:**

- En temelde üç veya dört ana rengin belirli oranlarda karıştırılmasıyla istenilen rengin elde edilebileceği düşünülebilir
  - RGB (Red-Green-Blue; Kırmızı-Yeşil-Mavi) karışımı ile renkleri ifade etme.
  - CMY (Cyan-Magenta-Yellow; Turkuaz-Kızılımsı Mor-Sarı), ayrıca
    CMYK renk uzayında K (Siyah) bileşen de eklenerek siyah bulanıklığı
    giderilmiştir.
  - HSI, HSB veya HSV (Hue-Saturation-Intensity, Brightness veya Value; Renk
    Özü-Doygunluk, Yoğunluk, Parlaklık veya Değer)
  - YUV (Luminance, Chrominance 1, Chrominance 2)
  - YIQ (NTSC’ de kullanılan Luminance, Chrominance 1, Chrominance 2
    sistemi)
  - YCbCr (Luminance, Chrominance 1, Chrominance 2 kanallarının
    ayrıştırıldığı bir diğer sistem)

**HSV (Hue, Saturation, Value) veya HSB (Hue, Saturation, Brightness)**: Renk uzayı, renkleri sırasıyla **renk özü**, **doygunluk** ve **parlaklık** olarak tanımlar.

- **Renk özü (Hue):** Rengin baskın dalga uzunluğunu belirler, örneğin sarı, mavi, yeşil, vb.
- Açısal bir değerdir 0Â° - 360Â°, bazı uygulamalarda ise 0-100 arası olağanlaştırılır
- **Doygunluk (Saturation):** Rengin "canlılığını" belirler. Yüksek doygunluk canlı renklere neden olurken, düşük olasılık rengin gri tonlarına yaklaşmasına neden olur.
  - 0-100 arasında değişir.
- **Parlaklık (Value):** Parlaklık ise rengin aydınlığını yani içindeki beyaz oranını belirler.
  - 0-100 arasından değişir.

<center><image src="./image/hsv.jpg" width="700"></image></center>

<center><image src="./image/ycc.jpg" width="" height="100"></image></center>

**Görüntü Biçimleri:** Sayısal görüntüler çeşitli algılayıcılar tarafından
üretildikten sonra depolama alanlarında çeşitli dosya
biçimlerinde saklanırlar

- **İkili (Binary) Görüntüler:** İkili görüntülerde piksel değerleri sadece 1 veya 0 değeri alır.

  - Oluşturulan ikili görüntü herhangi bir resim dosyası
    olabileceği gibi, benzer objelerin işaretlendiği (varlığını veya
    yokluğunu gösteren) bir görüntü veya maskeleme gibi işaret
    işlemede yaygın olarak kullanılan yardımcı görüntüler
    oluşturulabilir

- **Gri Seviye Görüntüler:** Gri seviye görüntülerde kullanılan bit derinliğine göre (kullanılan bit sayısına göre) beyaz ve siyah arasındaki bütün gri yelpaze ifade edilir.

  - Örneğin 8-bit’lik derinliğe sahip gri seviye görüntü için 0 (00H) değeri siyahı ifade ederken 255 (FFH) değeri beyazı ifade eder.
  - 0 ile 255 arasındaki bütün değerler en koyu tondan en açığına kadar gri seviyeleri belirtir

- **RGB Renkli Görüntüleri:** Renkli görüntülerin oluşturulabilmesi için en az üç renk bileşeni veya parlaklıkla beraber iki renk bileşeninin kullanılması gerekmektedir. **Gri seviye= R\*0.3 + G\*0.59 + B\*0.11**

  - Renkli görüntülerin oluşturulmasında her biri farklı bir görüntü bandını ifade eden 2 boyutlu görüntü katmanları (layer veya plane) kullanılır.
  - Bu katmanların hepsi birlikte düşünüldüğünde aslında 3 boyutlu bir görüntü küpünü oluşturmaktadır.

**Görüntü Dosyaları:** Görüntü dosya biçimlerinde sadece parlaklık değerlerinin saklandığı herhangi bir sıkıştırma yapılmamış tipteki dosyalar RAW olarak adlandırılır.

- RAW dosyaları gri-seviye veya renkli görüntülerden oluşabilir. Bu tür
  dosyalarda bir başlık (header) bulunmaması durumunda görüntü dosyasının
  boyutu şu şekilde bulunabilir:

- **Görüntü dosya boyutu = Toplam piksel sayısı \* Katman sayısı \* Bit derinliği**

- RGB RAW tipinde 256 piksel genişliğe, 256 piksel yüksekliğe, 16
  bit/piksel derinliğe sahip bir görüntünün hafızada kaplayacağı alan

<center><image src="./image/islemboyut.jpg" width="700"></image></center>

- Bu durumda RAW dosyanın hafıza biriminde kaplayacağı alan 3145728
  bit=393216 byte= 384 kByte olarak hesaplanır.

- **Görüntü Dosya Tiplerinde Sıkıştırma:** Görüntü dosyalarında parlaklık ve renk bileşenlerinin bellekte daha az yer kaplamaları için herhangi bir sıkıştırma algoritması uygulanabilir.
- Örneğin, BMP dosyaları sıkıştırma işlemi gerçekleştirilmeden saklanırlar
- Genelde takip edilen yöntemde ise, sıkıştırma işleminin sağladığı dosya boyutu avantajı nedeniyle sıkıştırılmış dosya biçimleri daha çok tercih edilir.

- **Kayıplı - Kayıpsız Görüntü Sıkıştırma:**

  - **Kayıpsız Sıkıştırma Algoritmaları:** Görüntü sıkıştırıldıktan sonra görüntünün orijinal değerlerinin korunduğu ve aynen elde edilebildiği algoritmalardır.(Run Length Encoding, Huffman, LZW yöntemleri)
  - **Kayıplı Sıkıştırma Algoritmaları:** Görüntü sıkıştırıldıktan sonra
    görüntünün orijinal değerleri tekrar elde edilemez. Sıkıştırma
    sonucunda orijinal değerlere en yakın yaklaşıklıkla görüntü tekrar
    oluşturulur.(JPEG, MPEG)

- **Yaygın Görüntü Biçimleri:** BMP, JPEG, TIFF, PNG, GIF, PCX, ICO, PBM, PGM, PPM, PSD,
  JPEG

# <center>GÖRÜNTÜ İŞLEMEDE KULLANILAN TEMEL YÖNTEMLER</center>

**Görüntünün Negatifi:** Bir görüntüyü koordinat düzlemi üzerinde iki boyutlu bir
matris gibi düşünürsek, bu matrisin her bir elemanı görüntüdeki bir piksele karşılık gelmektedir

- O zaman resimde (x,y) koordinatında bulunan piksel I(x,y) ile gösterilebilir. I(x,y)=a ifadesindeki a ise (x,y) koordinatındaki pikselin değerini göstermektedir.
- Bir görüntünün negatifini almak için piksel değeri 255’ten çıkarılır. I(x,y)=a ise negatifini alınca oluşacak görüntünün piksel değerleri I'(x,y)=255-a olmalıdır.

**Görüntü Ters Çevirme:** Koordinat sisteminde bir matris gibi düşündüğümüz görüntüde

- En üstteki satır en alta en alttaki satır ise en üste getirilecek şekilde, satırlar tersten düzenlenirse görüntü ters çevrilmiş olacaktır
- Bunu x eksenine göre simetri olarak da düşünebiliriz.
- Formal olarak ifade etmek istersek H yüksekliğe sahip bir görüntüde (x,y) koordinatındaki piksel (H-x,y) koordinatına taşınmalıdır.

**Görüntü Aynalama:**

- Bu durumda; en sağdaki sütun en sola, en soldaki sütun ise en sağa gelecek şekilde tersten düzenlenmelidir.
- Bunu y eksenine göre simetri olarak da düşünebilirsiniz.
- Formal olarak ifade etmek istersek W genişliğe sahip bir görüntüde (x,y) koordinatındaki piksel (x,W-y) koordinatına taşınmalıdır.

**Görüntü Döndürme:** Görüntünün (x0,y0) merkez noktasına göre θ derece döndürülmesi ile (x,y) koordinatında bulunan bir noktanın (x1,y1) noktasına taşındığını düşünürsek, aradaki ilişki şu
şekilde olacaktır.

<center><image src="./image/dondurme.jpg" width="500"></image></center>

- Burada θ = 180 seçilirse, görüntü ters çevrilmiş olacaktır.
- Bu yöntemin dışında çeşitli yöntemler de vardır: “bi-kübik, en yakın nokta, bi-lineer”

**Görüntü Öteleme:** Bir görüntünün yatayda A, dikeyde B piksel taşınması (ötelenmesi) isteniyorsa; tüm pikseller (A,B) miktar kaydırılır.

- Yani (x,y) koordinatında
  bulunan bir piksel
  (x+A , y+B)
  noktasına taşınmış olmalıdır

**Görüntü Yakınlaştırma:** Amaç görüntünün olduğundan biraz daha
büyük gösterilmesini sağlamaktadır. Yazılımsal olarak yapılan yakınlaştırma işlemi, yakınlaştırma durumuna göre görüntülerde bozulmalara yol açar. Uygulanacak yöntemlerin birinde bir piksel büyütüldüğündeki resimde çevresindeki piksellere yetiştirilir.

<center><image src="./image/yakinlastirma.jpg" width="500"></image></center>

- Bahsedilen yöntemde,görüntü oldukça hızlı bozulur ve keskin geçişler yaşanır. Bunu önleyebilmek için yandaki gibi bir işlem yapılabilir. Böylece bozulma oranı daha az belli olacak şekilde yapılmış olur:

<center><image src="./image/yakinlastirma-formul.jpg" width="500"></image></center>

**Görüntü Uzaklaştırma:** Görüntü uzaklaştırma, bir resmin olduğundan küçük gösterilmesi işlemidir. Bu işlemde pikseller arasındaki ilişkiye göre yeni piksel değerleri belirlenir. Böylece görüntü boyutu küçültülmüş olur

<center><image src="./image/uzaklastirma.jpg" width="500"></image></center>

**Görüntü kaykılma (shear):**

<center><image src="./image/kaykılma.jpg" width="500"></image></center>

- Tüm dönüşüm formüllerini tek bir ifadeye dönüştürürsek :
  x’=ax+by+c
  y’=dx+ey+f

**Birleşik dönüşümler:** Birleşik dönüşüm matrisleri her bir dönüşüm
matrislerinin ard arda çarpılması ile elde edilir.

<center><image src="./image/birlesikdonusumler.jpg" width="500"></image></center>

**Aritmetik İşlemler:** Görüntülerin karşılıklı olarak aynı koordinata denk gelen
piksellerin değerleri arasında işlemler yapılır

- Bunu I3 (x,y) = I1 (x,y) + I2 (x,y)şeklinde ifade edebiliriz (Burada toplama dışında diğer işlemlerde yapılabilir).

<center><image src="./image/aritmatiktoplama.jpg" width="500"></image></center>

**Mantıksal İşlemler:** Arka planın 0, ön planın 1 ile ifade edildiği ikili resimlerde mantık işlemlerini uygulayabiliriz.

- Uygulayacağımız işlemler VE, VEYA ve DEĞİL’dir. VE ile
  VEYA işlemlerinde matrislerin karşılıklı koordinatlarında
  bulunan pikseller bu işlemlere tabi tutulur.
- DEĞİL işleminde ise matristeki tüm sıfırlar bir, tüm birler sıfır
  olarak ayarlanır.

<center><image src="./image/mantiksal.jpg" width="500"></image></center>

**Uzamsal Süzgeçlemenin Temelleri:** Resim üzerinde yapılacak uzamsal işlemlerde komşuluk ilişkileri dikkate alınır

# <center>GÖRÜNTÜ İYİLEŞTİRME YÖNTEMLERİ</center>

**Görüntü Parlaklığı:** Parlaklık ayarı verilen görüntünün her bir piksel değerinin belirli bir sayıyla toplanması (veya çıkarılması) ile
yapılmaktadır.

- Formal olarak ifade edersek (x,y) koordinatında bulunan
  piksel için işlem şu şekilde olmaktadır: I'(x,y) = I(x,y) + K

- Eğer pozitif bir değer ise parlaklık artar, negatif bir değer ise
  parlaklık azalır

**Görüntü Karşıtlığı:** Karşıtlık (kontrast) ayarı, verilen görüntünün her bir piksel değerinin belirli bir sayıyla çarpılması ile yapılmaktadır

- Formal olarak ifade edersek (x,y) koordinatında bulunan
  piksel için işlem şu şekilde olmaktadır: I'(x,y) = A \* I(x,y)

- Eğer pozitif bir değer ise karşıtlık artar, negatif bir değer ise karşıtlık azalır.

**Histogram:** Histogram, sayısal bir resim içerisinde her renk değerinden kaç adet olduğunu gösteren grafiktir.

- Histogram üzerine uygulanabilecek iki temel işlem vardır.
  - Histogram germe
  - Histogram eşitleme

**Histogram Yorumları:**

- Eğer resim koyu ise [0,127] aralığındaki piksel değerleri
  fazlaca bulunacağından; histogram grafiklerinin sol
  tarafında yoğunlaşma olmaktadır

- Eğer resim açık ise [128,255] aralığındaki piksel değerleri fazlaca
  bulunacağından; histogram grafiklerinin sağ tarafında yoğunlaşma
  olmaktadır

- Benzer şekilde resmin kontrast ayarı düşük ise histogram belli bir bölge
  toplanmış olacaktır. Kontrast ayarı arttırıldıkça histogram grafiği daha
  geniş bir alan kaplamaya başlar.

**Görüntü Karşıtlığının Yayılması (Histogram Germe):**

- Karşıtlık yayma işlemi, bir görüntü üzerindeki en düşük ve en yüksek piksel değerlerine göre resmin düzenlenmesi işlemidir
- Bu işlemin genel formülünde; en küçük değer 0, en büyük değer 255 değerine çekilir ve diğer piksel değerleri ise bu aralıkta olması gereken değeri alır.
- Bu değer aşağıdaki gibi bulunur: (max: en büyük değerli pikselin değeri, min: en küçük değerli pikselin değeri)

<center><image src="./image/histogramgermeformul.jpg" width="250"></image></center>

- Histogram germe doğrusal bir dönüşümdür. Bu nedenle resmin histogramını düzenlerken içerisindeki verileri daha çok korur
- Histogram germe için aşağıdaki formül kullanılır.
- Burada a resim içerisindeki en küçük değerli pikselin değerini, b ise an büyük değeri göstermektedir. A değeri yeni resimde oluşması istenen en büyük B değeri ise oluşması istenen en küçük değerlerdir..
- Histogram eğrisini 0-255 arasına germek için A=255 B=0 seçilmelidir

<center><image src="./image/histogramgermeformul2.jpg" width="250"></image></center>

**Histogram Eşitleme:** Bir görüntünün renk değerlerinin belli yerlerde kümelenmiş
olmasından kaynaklanan renk dağılım bozukluğunu gidermek
için kullanılır.

- Böylece çok kullanılan pikseller belirgin hale dönüşmüş olur.
- Amaç: resimdeki düşük görünürlüğü iyileştirmek
- Olasılık dağılımına bağlı olarak doğrusal olmayan dönüşüm gerçekleştirilir
- Görüntüde bulunma olasılığı yüksek pikseller arası fazlaca açılırken (geniş alana)
- Düşük olasılıklı seviyeler birbirine daha yakın hale (dar alana) gelir
- Bu sayede daha çok kullanılan piksel değerleri daha görünür hale getirilir

**Histogram Eşitleme Özeti:**

<center><image src="./image/histogramesitlemeformul.jpg" width="300"></image></center>

1. Resimin histogramı bulunur.
2. Histogramdan yararlanılarak kümülatif histogram bulunur. Kümülatif histogram, histogramın her değerinin kendisinden öncekiler ve kendisinin toplamı ile elde edilen değerlerin içeren büyüklüktür.
3. Kümülatif histogram değerleri normalize edilip (toplam piksel sayısına bölünerek), yeni resimde olmasını istediğimiz max. renk değerleri ile çarpılır, çıkan değer tam sayıya yuvarlatılır. Böylelikle yeni gri seviye değerleri elde edilmiştir.
4. Eski (Orjinal) gri seviye değerleri ile; 3. adımda elde edilen ri seviye değerleri biribirine karşılık düşürülür ve yeni histogram grafiği çizilir.

n: Giriş görüntüsündeki toplam piksel sayısı (n<sub>0</sub>+n<sub>1</sub>+ .... +n<sub>L-1</sub> = n)

n<sub>j</sub>(n<sub>k</sub>): j. gri seviyedeki piksel sayısı

L: mümkün olan (veya istenilen) toplam gri seviye sayısı (8 bit renk derinliğinde 255 vb.)

s<sub>k</sub>: Daha iyi kontraslı bir görüntü elde etmek için gri seviye dönüşüm değeri.

# <center>Renk Dönüşümleri ve Dönüşüm Matrisi</center>

**Renk Dönüşümleri ve Dönüşüm Matrisi**

- Renkler görüntüleri oluşturan temel kavramlardır. Işığın bir cisme çarpıp
  belirli dalga boylarının soğrulması ve belirli dalga boylarını yansıtılması ile gözümüzde renk algısı oluşur
- Amacımız bu 3 kanalı kullanarak yeni bir renk elde etmek.
  Bunu yapmak için basit olarak yandaki denklemi yazabiliriz

<center><image src="./image/renkdonusum.jpg" width="200"></image></center>

- Bu denklemde sırasıyla a, b, c yeni oluşturulan renkte kırmızı, yeşil ve mavi kanalın katkısını, d ise ifadeyi genelleştirmek için kullanılan ve bu katkılara ek olarak sabit bir değer ile toplama işlemini modellemek için kullanıldı.
- Burada Y dönüşüm sonucu oluşan yeni resimdeki bir renk kanalını göstermektedir
- Renkli her resimde 3 kanal (RGB) bulunduğundan, yukarıda verilen eşitliği bir 3x4 bir matrisyardımıyla ifade etmek mümkündür.
- Görülen dönüşüm matrisi bir resmin RGB kanalları kullanılarak, lineer işlemler sonucu elde edilebilecek tüm sonuçları alabilmemizi sağlayacak genel bir yapıdadır

<center><image src="./image/donusummatrisi.jpg" width="300"></image></center>

**Kanal Ayırma:** Bu işlemde resme ait RGB kanalları tek tek ayrılarak, her bir kanalın özgün katkısı incelenmiştir

- Burada dikkat edilecek bir nokta, mavi kanalda detaylar çok az
  belirginken, yeşil kanalda detayların çoğunun görünür olduğudur.
- Bunun en önemli sebebi; gözümüzün mavi ışığın var olduğu dalga boyuna daha az hassas olmasıdır.
- Yani aynı gri seviye görüntüyü mavi ve yeşil olarak renklendirirsek,
  yeşil kodlanan görüntü gözümüze daha fazla bilgi içeriyor şeklinde örünecektir
- Gece görüş sistemlerinde yeşil renk görüntü verilmesinin temel sebebi de
  budur.

<center><image src="./image/kanal.jpg" width="500"></image></center>

**Kanal Çevirme**

- Kanal çevirme de görüntü işlemede ender kullanılan basit dönüşümlerden biridir.
- Mantık herhangi bir kanalın değerini 255 e tümleyenine çevirmektir.

<center><image src="./image/kanalcevirme.jpg" width="500"></image></center>

**Gri Seviye Dönüşümü:**

- Gri, RGB kanallarından üçünün de aynı değere sahip
  olduğunda oluşan bir renktir
- Hangi katsayıları kullanırsak kullanalım R'G'B' değerlerini aynı
  yaptıktan sonra oluşacak görüntü gri seviyedir.

<center><image src="./image/gridonusum.jpg" width="500"></image></center>

**Sepya Dönüşümü:**

- Sepya günümüzde sıklıkla kullanılan, kırmızı ve yeşilin çok
  hafif tonlarından oluşmuş, gri seviye benzeri bir
  tonlamadır

<center><image src="./image/sepya.jpg" width="500"></image></center>

**Renk Dönüşümleri**

- Bahsedilen dönüşüm matrisi tanımlanan işlemleri renk
  kanallarına uygulamaktadır
- Bunun dışında daha farklı görüntüler ve filtreler oluşturmak için, pikselden piksele (noktasal) dönüşüm yapılır
- Pikselden piksele dönüşüm 2 farklı şekilde gerçeklenebilir

  - Belirli bir ton -----> Belirli bir tona
  - Belirli bir noktadaki ton ------> Aynı noktadaki farklı bir
    tona

- Nokta-nokta dönüşümü ile resmin renkleri üzerinde yalnızca piksel koordinat değerlerine bağlı bir dönüşüm işlemi tanımlanır. Bunu önceki mantığa benzetmek adına,renk tonuna değil piksel koordinatlarına özgü bir renk dönüşümü olarak düşünebiliriz.
- Renk dönüşümüne benzer olarak, her bir piksel üzerindeki rengin atanması gereken yeni rengi gösteren bir dönüşüm haritası oluşturulur.
- Burada anlatılacak olan işlem görüntü işleme literatüründe **image blend** (görüntü karıştırma) olarak geçmektedir
- Aynı boyutlarda (genişlik ve yükseklik) iki görüntünün (yada bu konseptte katmanın) bir biri ile matematiksel bir işlem aracılığı ile karıştırılması işlemidir.

**Doğrusal Toplam:**

- f(x,y) = ax+(1-a)y
- İki resmin belirli ağırlıklarla (a,1-a) birbirine karıştırılması işlemidir.

**Çarpma:**

- f(x,y) = xy
- Karşılıklı iki pikselin çarpılması ile yeni görüntü elde edilir.

**Aydınlatma:**

- f(x,y) = max(x,y)
- Adından da kolaylıkla anlaşılabileceği gibi aydınlatma iki katmanı her nokta için en büyük değeri seçerek birleştirir

**Karartma:**

- f(x,y) = min(x,y)
- Karartma aydınlatma işleminin tersi olarak tanımlıdır ve yeni görüntü iki katman içerisindeki en düşük noktalar aracılığı ile oluşturulur

**Kaplama:**

- f(x,y) = (x<0.5) ? (2xy) :(1-2(1-x)(1-y))
- Kaplama karıştırma işlemleri içerisinde en sık kullanılan işlemlerden biridir ve üst katmanı alt katmanın üzerine kaplama etkisi verir

# <center>UZAMSAL GÖRÜNTÜ İŞLEME</center>

**Uzamsal Süzgeçlemenin Temelleri:** Resim üzerinde yapılacak uzamsal işlemlerde komşuluk ilişkileri dikkate alınır

- Böylece kenar bilgisi, gürültü bilgisi gibi bilgiler daha anlamlı hale gelmiş olur
- Bir pikselin komşularını da dikkate alarak yapılan hesaplamaları **süzgeçleme** denilmektedir.
- Süzgeç kelimesi; çeşitli kaynaklarda **filtre**, **maske**, **kernel** **pencere** şeklinde de ifade edilmektedir.

**Uzamsal İlişki ve Konvolüsyon:** Piksellerin uzamsal komşulukları, matris şeklinde ifade edilmektedir. Pikseli matrisin (filtre) ortasına gelecek şekilde ayarladığımızda etrafındaki pikseller, o pikselin uzamsal komşuları olmaktadır

- Örneğin 3x3’lük bir matris(filtre) düşündüğümüzde pikselin çevresinde
  kalan piksel onun uzamsal ilişkili komşularını göstermektedir.
- Merkezdeki pikselden uzaklaşılacağı için bilgiyi anlamsızlaştırır. Bu yüzden genelde 3x3 veya 5x5’lik matrisler içindeki komşuluk ilişkileri kullanılmaktadır.
- Süzgeç matrisleri içerisinde pikselin hesaplama için olan anlamını gösterecek sayılar yer alacaktır
- Süzgeç kullanarak tüm piksellerin işleme alınmasına **konvolüsyon** denilmektedir.

<center><image src="./image/suzgec.jpg" width="500"></image></center>

- Sol şekilde I resmindeki I(x,y) pikselinin komşuları gösterilmiştir.
  Sağ tarafta ise 3x3’lük bir süzgeç gösterilmektedir.

- Bu süzgecin 5 numaralı hücresi I(x,y) üzerine gelecek şekilde tutulduğunda, karşılıklı hücreler çarpılır ve tüm çarpımlar toplanır
- I'(x,y) = 1 x I(x-1, y-1) + 2 x I(x-1, y) + 3 x I(x - 1, y + 1) + 4 x I(x , y - 1) + 5 x I(x,y) + 6 x I(x , y + 1) + 7 x I(x +1, y - 1) + 8 x I(x + 1, y) + 9 x I(x + 1, y + 1)

- Böylece her bir hücre, süzgeçte karşısına gelen katsayı ile çarpılır.
  Çarpımlar toplanarak yeni oluşan resmin (x,y) koordinatına
  yazılır

- Bu işlemin tüm piksellere uygulanmasına konvolüsyon (katlama)
  denilmektedir. Süzgecin matrisine K dersek;
  I'(x,y) = I(x,y) \* K şeklinde ifade edilmektedir.

**Uzamsal Süzgeç Maskelerinin Oluşturulması:** Maskeler oluşturulurken, yapılacak işlemin özellikleri dikkate alınmalıdır

- Örneğin yatay kenar bilgisi ön plana çıkarılmak
  isteniyorsa, hücrenin sağındaki ve solundaki pikseller
  anlamlıdır. Sağa çapraz kenarlar incelenmek isteniyorsa,
  hücrenin sağ köşegenindeki pikseller anlamlıdır

**Ortanca Süzgeci:**

- Maskeler ile resimler matematiksel hesaplamalar olmadan da katlanabilmektedir
- Bu tip süzgeçlere verilecek en önemli örnek ortanca (median) süzgecidir
- Ortanca, bir grup sayı dizisinin ortasında yer alan sayıyı ifade etmektedir (süzgeç matrisindeki sayılarla işlem yapmadığımıza dikkat ediniz)

<center><image src="./image/ortanca.jpg" width="500"></image></center>

- Örneğin resim katlamak (konvolüsyon işlemi) için seçtiğimiz pencere 3x3'lük bir süzgeç olsun. Bu pencerenin karşılık geldiği 9 sayı sıralanır ve ortadaki eleman yeni resmin pikseli olarak yazılır. Böylece matematiksel işlem yapmadan yeni bir resim elde edilmiş olur. Bu işlem sayesinde, resimlerdeki gürültüler yüksek ölçüde azaltılmış olmaktadır.

<center><image src="./image/süzgec.jpg" width="500"></image></center>

**Ortalama Süzgeci:**

- Bu süzgeçte piksel değeri, süzgeç ile belirlenen komşuları ile toplanır ve ortalaması alınır
- Bu filtre ile resimdeki bazı gürültüler silinirken; resimde yumuşak geçişler olmaktadır.

**Yumuşatan Uzamsal Süzgeçleme:**

- Matrisindeki elemanların pozitif olduğu süzgeçler; resim
  ile katlandığında (konvolüsyona sokulduğunda) oluşan
  resimde geçişler daha yumuşak olur.

- Bu tip süzgeçlere alçak geçiren süzgeç ya da **yumuşatan süzgeç** denir

- Bu süzgeç sayesinde resimdeki aşırı ışık, normal seviyelere
  çekilerek **normalizasyon** yapılmış olur.

- Bu işlem ile aynı zamanda ortalama alma işlemi
  gerçekleştirilir. Süzgeçteki tüm elemanlar pozitif
  olduğundan, sonucu tekrar [0,255] aralığına alabilmek
  için konvolüsyondan çıkan sonuç süzgeçteki
  elemanların toplamına bölünmüş olur.

- Böylece ortalaması bulunan değer gerekli pikselin
  olduğu yere yazılır

<center><image src="./image/ortalamasuzgec.jpg" width="500"></image></center>

**Keskinleştiren Uzamsal Süzgeçleme:** Matrisindeki elemanların pozitif ve negatif değerler içerdiği süzgeçler; resim ile katlandığında oluşan resimde
yüksek frekanslı (keskin hatlar) ön plana çıkar

- Bu tip süzgeçlere yüksek geçiren süzgeç ya da keskinleştiren
  süzgeç denir

- Bu süzgeç sayesinde resimdeki kenar bilgileri, keskin hat
  değişiklikleri vs. bulunmuş olur.

<center><image src="./image/keskinkenar.jpg" width="500"></image></center>

**Kenar Belirleme Yöntemleri:** Resim üzerinde renklerde meydana gelen ani değişimlere kenar denilmektedir. Kenar bulma işlemi resimler
üzerinde sık uygulanan bir işlemdir

- Bu işlem için öncelikle resimdeki gürültü ortanca süzgeci
  ile temizlenir, sonrasında ise yüksek frekanslı süzgeçler
  kullanılarak kenarlar pekiştirilir.

- Kenar bulma ile ilgili çeşitli süzgeçler mevcuttur. **Prewitt**
  ve **Sobel** süzgeçleri bu süzgeçlerden en çok kullanılanlarındandır.

**Prewitt Yöntemi**

<center><image src="./image/prewitt.jpg" width="300"></image></center>

- Dikey veya yatay kenarlar dışında, tüm yönlerde olabilecek kenarları şu şekilde bulunur. Yatay Prewitt kenar süzgecinden gelen sonuç Gx, dikey Prewitt kenar süzgecinden de gelen sonuç Gy olsun. Konvolusyon işleminin sonucu

<center><image src="./image/prewitthesap.jpg" width="200"></image></center>

**Sobel Yöntemi**

<center><image src="./image/sobel.jpg" width="300"></image></center>

- Dikey veya yatay kenarlar dışında, tüm yönlerde olabilecek kenarları şu şekilde bulunur: yatay Sobel kenar süzgecinden gelen sonuç Gx , dikey Sobel kenar süzgecinden de gelen sonuç Gy olsun. Konvolusyon işleminin sonucu

<center><image src="./image/prewitthesap.jpg" width="200"></image></center>

**Uzamsal SüzgeçlemeYöntemleri ile Görüntü Zenginleştirme**

- Görüntü zenginleştirme, bir görüntünün daha anlaşılır ve
  yorumlanabilir hale gelmesini sağlamaktır. Görüntüler
  pek çok histogram işlemleri ve filtreleme metotları ile
  zenginleştirilebilir

- Histogramlar ile belli dağılıma sahip piksel değerleri
  üzerinde işlem yapılarak görüntü daha belirgin hale
  getirilir. Karşıtlık ayarları üzerinde oynama yapılarak
  görüntü daha belirgin hale getirilir

- **Alçak geçirgen filtre:** Görüntü kalitesini bozan gürültü
  ve parazitleri giderir. filtre bir görüntüyü yumuşatır
  ve görüntüyü genelleştirir

- **Yüksek geçirgen filtre:** Parazitsiz görüntülerde
  küçük cisimlerin ayırt edilebilmesini sağlar. filtre,
  kenarları ve ayrıntıları vurgular

**GAUSSİAN BLURRİNG FİLTRE (AĞIRLIKLI ORTALAMA):** AĞIRLIKLI ORTALAMA'da, maske içerisindeki gri tonlar belirli ağırlıklarla (coefficients(kat sayısı) ) çarpılır.

- **Gausian alçak geçiren filtre** ve normal ortalamanın
  ağırlıklarını gösterilmektedir.

- Maskenin şeklinden dolayı bu maskeyi kullanan filitreye kutu
  filitre denir

- Gaussian alçak geçirenin düzgünleştirme etkisi kutu
  filtreninkinden biraz daha iyidir. Fakat gri ton basamaklarının
  yassılaştırma problemi bunda da mevcuttur.

<center><image src="./image/gaussian.jpg" width="500"></image></center>

**Laplacian Filtre:**

- Laplas filitresi bastiçe bir resimdeki kenar
  hatlarını belirlemek için kullanılır. Burada
  kenar ile kastedilen objeleri genelde arka
  plandan ayıran keskin renk ayrılıklarıdır.
  Keskinleştirme Filitresi (Sharpening Filter)
  ismi ile de anılan laplas filitresi çalışırken bir
  pencere kullanır

<center><image src="./image/laplasfiltre.jpg" width="200"></image></center>

- Bir görüntü Laplace filtresi ile konvolüsyon yapılır ve orijinal görüntüden çıkartılırsa keskinleştirme operatörü elde edilir.

<center><image src="./image/keskinlestirme.jpg" width="400"></image></center>
