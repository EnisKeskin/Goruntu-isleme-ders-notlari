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

# BÖLÜTLEME YÖNTEMLERİ

- Bölütleme, **görüntüyü birbirine benzer alt bölgelere
  ayırma işlemidir.** Bir diğer bakış açısıyla görüntü verisinin
  bileşenler cinsinden daha özet bir şekilde sunulmasını
  sağlamaktır.
- Bu bakış açısıyla bakacak olursak görüntüyü anlamlandırmak ve **bize gereken bilgiyi görüntüden elde etmek için kullanılabilecek temel bir görüntü işleme başlığıdır denilebilir.**

## Bölütleme Kavramı

- Bölütleme kavramı oldukça büyük bir alanı kapsamaktadır.
  Temel olarak bölütlemede çıkarılması** istenen görüntü
  bileşenlerinin ortak bir görsel niteliğe sahip olması** gerektiği
  varsayılmaktadır.

- Görüntüde birbirine benzer pikseller, nesneler, dokular
  ayrıştırılarak birbirleriyle de bölgesel olarak **‘alakalı’** bölüt
  parçaları oluşturulabilir.

- Bölütleme, tıbbi görüntülemede, biyometrik tanımada, makine
  görmesi uygulamalarında, güvenlik amacıyla kişi takibi, yüz
  tanıma, uzaktan algılamada farklı maddelerin tespiti gibi
  uygulamalarda kullanılmaktadır.

## EşiklemeTabanlı Bölütleme - Görüntü Eşikleme

- Bir görüntüden, belli bir değere göre ikili resim elde edilmesi işlemidir
- Bu değere **Eşik değeri** denir
- Bir piksel eşik değerinden büyük ise 1, küçük ise 0 değeri yazılır.
- Böylece ikili resim elde edilmiş olur.

## Eşikleme Tabanlı Bölütleme

- Eşikleme yöntemi ile bölütlemede, gri seviye görüntülerin
  piksel seviyelerinin belli bir eşik değerin altında veya
  üstünde olmasına göre ikili (binary) olarak karar verilerek
  ikili görüntüler oluşturulur.
- Ayrıca birden fazla, Nth adet eşik seviyesinin belirlenmesi
  durumunda görüntü toplam Nth + 1 farklı bölüte ayrılır.
- Eşik seviyesinin belirlenmesinde k-ortalamalar, bulanık cortalamalar gibi kümeleme yöntemlerinin yanı sıra Otsu
  yöntemi, maksimum entropi yöntemi v.b. yöntemler
  yaygın olarak kullanılmaktadır.

## Görüntü Eşikleme (Image Tresholding)

- Eşikleme yada ikili tonlama gri tonlanmış bir resmin siyah-beyaz (ikili) uzaya dönüştürülmesi işlemidir.
- Siyah-beyaz görüntüler, görüntü üzerindeki renklerin pek önemli olmadığı, görüntü üzerinde belirli şekillerin veya dizilerin arandığı uygulamalarda işlem yükünü hafifletmek ve görüntü üzerinde mantıksal (0-1) işlemleri hızlı bir şekilde yapabilmek için sıklıkla kullanılan görüntülerdir.
- Basitçe gri seviye bir görüntü üzerinde 0-255 arasında seçilen bir T eşik değerine göre,siyah-beyaz resim aşağıdaki şekilde oluşturulur.

<center><image src="./image/teml.png" width="400"></image></center>

## Görüntü Eşikleme (Image Tresholding)

- Burada T değerinin doğru seçilmesi kritik önem
  taşımaktadır.
- Eğer T değeri çok büyük seçilirse
  oluşturulacak yeni görüntüde pek çok piksel beyaz (1),
  küçük seçilirse de siyah (0) olacağından görüntünün
  içerdiği bilgi ciddi miktarda azalacaktır.
- Birkaç resim için
  ideal eşik değeri deneme yoluyla bulunabilse de farklı ışık
  ortamlarında çekilmiş çok sayıda görüntü için bu söz
  konusu olamaz.
- Bu nedenle girdi resmine karşılık eşik
  değerini otomatik olarak hesaplayan bir algoritma
  gerekmektedir.

## Otsu ile Adaptif Eşikleme

- Otsu metodu ile eşik değeri görüntü üzerinden
  hesaplanmaktadır.
- Metod, görüntü üzerinde iki ayrı sınıf (plan) olduğunu
  kabul ederek, bu iki sınıf arasındaki varyansı
  maksimum yapacak değeri bulmaya çalışır
- Varyans bir dizinin elemanlarının dizinin ortalamasına
  olan uzaklıklarının karelerinin ortalamasıdır. Bu değere
  bakarak dizi içerisindeki değerlerin ortalamaya ne
  derece yakın olduğu görülebilir.

## Otsu ile Adaptif Eşikleme

- N uzunluklu bir dizi için varyans,
<center><image src="./image/otsu.jpg" width="400"></image></center>

- Sınıflar arası varyans(siyah-beyaz sınıfları) aşağıdaki formül ile bulunur.
-

<center><image src="./image/otsu1.jpg" width="400"></image></center>

- Burada w değişkenleri sınıf yoğunluklarını, µ değişkenleri ise ağırlıklı sınıf
  ortalamalarını göstermektedir. i renk değerini, p(i) ise o rengin olasılığını ifade
  etmektedir. L ise max renk değeridir.

<center><image src="./image/otsu2.jpg" width="400"></image></center>

- t=0 ilk değer ile başlayarak 255 e kadar her değer için sınıflar arası varyansı
  hesaplamakta ve en son maksimum varyans değerini veren t değerini T (eşik
  değeri) olarak belirlenmektedir

- İkinci resim T=75 eşik değeri ile eşiklendiğinden yüz
  kısmında bulunan pek çok veri kaybolmuş, üçüncü resim
  yüksek bir eşik değeri T=180 ile eşiklendiğinden
  neredeyse tüm bilgiler kaybolmuştur. Son resim ise
  adaptif eşik değeri bulunarak T=115 eşiklenmiştir ve
  resim üzerindeki pek çok bilgi korunmuştur.

## Kenar Belirleme Tabanlı Bölütleme

- Bir görüntüde bölütlenmek istenen farklı nesnelere ait kenarlar
  bölüt sınırlarının oluşturulmasında kullanılabilir.
- Bir nesneden diğer
  bir nesneye geçerken veya bir nesne ile arka plan geçişleri arasında
  keskin geçişler oluşur.
- Kenar belirleme algoritmaları ile kenarlar
  belirlendikten sonra üç işlemin gerçekleştirilmesi gerekmektedir:
- Kenarlarda oluşan kopuklukların giderilmesi
- Hangi kenarların bölüt sınırlarını oluşturduğuna karar verilmesi
- Aşırı kenar oluşması durumunda (nesnelerin yüzeylerinin benzeşik
  (homogenous) olmaması durumunda) gerçek sınır kenarlarının tespiti.
- Ayrıca bölütlenmek istenen **nesnenin şekil özelliklerine** göre çizgi
  veya yuvarlak yapıların bulunabilmesi için **Hough**, yönlendirilmiş
  **Sobel** ve **Leavers** dönüşümü gibi çeşitli dönüşüm yöntemlerinden de
  yararlanılır.

## Histogram Tabanlı Bölütleme

- Histogram tabanlı yöntemlerde görüntüdeki tüm pikseller hesaba katılarak
  oluşturulan histogramda bulunan vadi ve tepelerden yararlanılarak oluşturulacak
  olan bölüt sayısı ve sınırları belirlenir.
- Görüntünün parlaklık veya renk histogramları
  ayrı ayrı değerlendirilerek bölütlerin oluşturulması sağlanır
- Bu noktada oluşturulan histogramda ‘mod analizinin’ iyi bir şekilde
  gerçekleştirilmesi gerekir.
- Daha alt bölütlerin bulunmaması veya görüntüdeki
  bölütlerin daha az olması istendiğinde histogram analiz algoritmasınının
  parametrelerinin daha ince veya kaba bir biçimde ayarlanarak istenilen sonuçların
  elde edilmesine çalışılır.
- Özellikle belirgin tepe ve vadi noktalarının oluşmaması durumunda bölütleme
  başarısı bundan olumsuz olarak etkilenebilir.
- Bu olumsuzlukları giderebilmek için
  istatistik özelliklerini de içeren ardışıl histogram analiz algoritmaları kullanılır

## Bölge Büyütme Tabanlı Bölütleme

- Görüntüdeki piksellerin ve bölgelerin daha önceden belirlenmiş bir koşula
  bağlı olarak gruplandırarak bölütlerin oluşturulduğu yöntemi bölge
  büyütme tabanlı bölütleme yöntemi olarak adlandırılır.
- Temel olarak görüntü içinden rastgele veya önceden belirlenerek seçilen
  çekirdek (seed) noktaların çevresindeki komşu pikseller belirli bir benzerlik
  ölçütüne göre gruplanarak, giderek yayılan bir şekilde yinelemeli olarak
  bölütler oluşturulur.
- Benzerlik koşulunun belirlenmesinde ele alınan
  problemin tipi ve yapısı oldukça önem kazanır.
- Bölütleme başarımı seçilen
  başlangıç çekirdeklerinin seçimine bağımlıdır.
- Gürültü ve dengesiz çekirdek
  seçimi bölütleme sonucunu olumsuz etkiler.
  Çekirdeksiz bölge büyütme algoritmasında ise çekirdeklerin açıkça
  seçilmesine gerek yoktur.
- Başlangıç olarak tek bir bölge veya pikselle
  bölütleme işlemine başlanarak her bir yinelemeli adımda komşu bölge veya
  piksellerin benzerliğini değerlendirir.
- Seçilen bir eşik değeri yardımıyla
  değerlendirilen bölge veya pikselin var olan bölgeye eklenip eklenmeyeceği
  veya yeni bir bölüt etiketi oluşturulup oluşturulmayacağına karar verilir.

## Bölme ve Birleştirme Tabanlı Bölütleme

- Bölge büyütme tabanlı görüntü bölütleme yönteminin tersine
  görüntü keyfi olarak keyfi ve bağlantısız alt bölgelere ayrıştırılır; daha
  sonrasında belirlenen bölütleme koşullarına bağlı olarak bu alt
  bölgeler birbirleriyle birleştirilerek veya bölünerek bölütleme
  haritası oluşturulmaya çalışılır.
- Bu yaklaşımda bütün görüntü bir ağacın kökünde kabul edilerek
  işleme başlanır.
- Bu ağaç yapısında belli bir benzerlik koşuluna göre
  ağaç alt dallara ayrıştırılır.
- Bu ayrıştırmada amaçlanan, ağacın her bir
  dalında birbiriyle yüksek oranda ilişkiye sahip, benzer bölgelerin veya
  piksel gruplarının toplanmasını sağlamaktır.
- Bu ayrıştırma işlemi
  yinelemeli olarak devam eder ve belli bir benzeşim değeri
  yakalandığında ağaç düğümlerinde bölütler oluşturulur.

## Kümeleme Yöntemleri ile Bölütleme

- Görüntü verisindeki benzer, doğal olarak birbirleriyle ilişkili bileşenlerin
  kümelenmesi mantığıyla bölütleme işlemi gerçekleştirilebilir.
- Bu durumda kümeleme iki yaklaşımla ele alınır:
  - Bölümleme (Partitioning): Görüntüyü geniş bir veri kümesi olarak düşündüğümüzde
    bu kümede ilişkili bileşenleri oluşturacağımız benzerlik modeline göre ayrıştırabiliriz.
  - Gruplama (Grouping): Görüntüdeki farklı saydığımız veri bileşenlerinin hangilerinin
    beraberce bir grup içinde yer almasına karar verilerek ‘gruplama’ mantığıyla
    kümelerimizi (alt bölütlerimizi) oluşturabiliriz.
- Bölütlemeyi gerçekleştirebilmek amacıyla örüntü tanıma ve makine
  öğrenmesi kapsamına giren kümeleme algoritmalarından yararlanılması
  oldukça yaygındır.
- Çoğu zaman görüntü bölütleme ve kümeleme kavramları iç
  içe kullanılır.
- Ama geniş yelpazeden bakacak olursak kümeleme yöntemleri
  bölütlemede kullandığımız yöntemlerden biridir.
- Görüntü bölütleme alanında en çok kullanılan eğiticisiz öğrenme yöntemleri
  olarak k-ortalamalar, bulanık c-ortalamalar, öz-düzenlemeli haritalar,
  uyarlanabilir rezonans teorisi algoritmalarını sayabiliriz.
- Bu yöntemlerden en sık kullanılan k-ortalamalar ve bulanık c-ortalamalar algoritmalarını genel hatlarıyla tanıyacak olursak:

## K-Ortalamalar Algoritması

- K-ortalamalar, görüntü işlemede doğal kümeleri yinelemeli
  olarak bulan bir kümeleme yöntemidir. K-ortalamalar algoritması
  toplam N pikselden oluşan veri setini kümeye ayırır.
- Kortalamalar algoritması çok boyutlu örneklerin oluşturduğu
  vektör uzayında küme içi değişintiyi karesel hata fonksiyonu ile
  minimize etmeye çalışır.
  Bu hata fonksiyonunda c , küme sayısını, Si , i = 1,2,3
  ....,c kümeleri, μi ise Si kümesindeki bütün veri noktalarının
  ortalamasını yani küme merkezini göstermektedir xj ∈ Si. Küme
  merkezleri aynı zamanda ‘sentroid (centroid)’ olarak da
  adlandırılır.
- K-ortalamalar algoritmasının işlem adımları aşağıdaki
  gibi özetlenebilir.

- Adım 1. Algoritmanın başlangıcında c küme merkezi rastgele
  oluşturulur. Veya daha küçük bir veri setinde k-ortalamalar
  algoritmasının uygulanması sonucu bulunan küme merkezleri başlangıç
  küme merkezi olarak atanır.
- Adım 2. Veri setindeki toplam N örneğe L2 normuna göre en yakın
  mesafede olduğu küme merkezine göre bir küme etiketi atanır.
- Adım 3. Küme merkezleri sahip olduğu bütün üye veri noktaları
  yardımıyla tekrar güncellenir.
- Adım 4. Si kümesine ait j örnek için (xj ∈ Si) şu hesaplamalar yapılır:
- Burada ny , y. kümeye ait örnek sayısıdır.
- Eğer ise j. örnek i. kümeden z. kümeye
  atanır. Her iki küme merkezi tekrar güncellenir.
- Adım 5. Eğer bir örnek son k. yinelemede Adım 4’te değiştirilmişse
  Adım 3’e gidilir, diğer durumda sonlandır.

## Model Tabanlı Bölütleme

- Model tabanlı bölütlemede, görüntüde bölütlenmek istenen
  nesnenin şekil yapısının olasılıksal bir model oluşturduğu
  düşünülür.
- Bu modelde ilgilenilen nesnenin tekrarlayan bir
  biçimi olduğu ve oluşturulan modelin belli kısıtlarla
  gerçeklenebileceği varsayılır.
- Model oluşturulurken
  bölütlenecek nesnelerin istatistiksel değişimleri öğrenilerek
  önsel (prior) model parametreleri çıkarılır.
- Model tabanlı bölütleme yöntemlerine en iyi örnekler aktif
  dış hatlar (active contours) ve şekiller (active shapes); seviyekümeleri (level-sets) ve biçim-değiştiren (deformable)
  modelleme yöntemleridir

## Çizge Bölümleme Yöntemleri

- Çizge bölümleme (graph partitioning) yönteminde başlangıç
  olarak bütün görüntü ağırlıklandırılmış ve yönlendirilmemiş
  bir çizge olarak oluşturulur.
- Görüntüyü oluşturan pikseller
  veya bölgeler bu çizgede düğümlerle ilişkilendirilir ve komşu
  piksel ve bölgeler arasındaki benzerlik ölçütü bu çizgedeki
  kenar ağırlıklarından yararlanılarak oluşturulur.
- Bu benzerlik
  kıstasını en-iyileyen (optimizing) bir model oluşturularak en
  iyi bölütlerin elde edilmesine çalışılır.
- Bu bölütleme türünde en iyi bilinen yöntemler olarak,
  minimum yayılan ağaç tabanlı bölütleme, minimum kesim,
  normalize kesimler,rasgele yürüyücü algoritmaları sayılabilir.

# GÖRÜNTÜ İŞLEMEDE MORFOLOJİK YÖNTEMLER

- Morfolojik işlemlerde amaç görüntüdeki nesnelerin
  belirginleştirilmesidir.
- Görüntüye uygulanması düşünülen kümeleme, özellik çıkarımı,
  sınıflandırma işlemlerinin başarılı sonuç verebilmesi için morfolojik
  işlemler büyük öneme sahiptir.
- **Birbirine değen nesnelerin ayırt edilmesi, önişleme sonucunda
  parçalı görünen nesnelerin birleştirilmesi, delik ihtiva eden
  nesnelerin boşluklarının doldurulması gibi işlemler morfoloji başlığı
  altında toplanmaktadır.**
- Morfolojik işlemler çoğunlukla ikili görüntülere uygulanmaktadır

## Aşındırma (Erosion)

- Aşındırma işlemi, ikili bir görüntüdeki nesnelerin
  küçülmesini, daralmasını sağlayan işlemdir.
- Bu işlem
  sonrasında görüntüdeki bazı gürültüler yok olur, nesneler
  arasındaki zayıf bağlantılar kaybolur.
- Arka plan olarak
  kabul edilen alan genişler.

## Genişletme (Ditation)

- Genişleme işlemi, aşındırma işleminin aksine nesnelerin
  büyümesini, genişlemesini sağlayan işlemdir.
- Görüntüde tek
  parça olması gereken bir nesne çeşitli işlemler sonucunda
  parçalı bir görünüme sahip olabilir veya tamamen ayrılabilir.
- Genişletme işlemi, yapısal elemanın türüne göre
  parçalanmanın onarılması veya ayrılan parçaların
  birleştirilmesi işlemini gerçekleştirmektedir.

## Yapısal Elemanlar

- Yapısal elemanlar, bir görüntüye morfolojik işlemlerin
  uygulanabilmesi için gerekli olan farklı yapı ve boyuta
  sahip ikili formattaki görüntülerdir.
- Uygulanacak işlemi
  yapısal elemanın türü belirler.

<center><image src="./image/yapisaleleman.jpg" width="400"></image></center>

- Morfolojinin temel amacı, daha önceden belirlenmiş bir piksel
  grubunu görüntü üzerinde gezdirip, ne kadarının uyduğu veya
  uymadığı durumunu incelemektir.
- Bunların bir merkez noktası bulunmakta olup, işlenecek resmin her
  bir pikseli bu noktaya oturtularak işlem yapılmaktadır.
- Genişleme ile görüntü içerisindeki objeler büyür veya kalınlaşır.
- Aşınmada ise tam tersi incelme veya büzülme olur.
- Operatörlerin etkileri yapıtaşı elemanının yapısına veya büyüklüğüne
  bağlıdır.

<center><image src="./image/gn.jpg" width="400"></image></center>

- Aşınma işleminde, yapıtaşı elemanının görüntü üzerindeki
  kısım ile tamamen uyuşması durumunda, yapıtaşı
  elemanının merkez noktası dışındaki yerler arka plan
  halini alır.

<center><image src="./image/as.jpg" width="400"></image></center>

## Örnek

- Verilen bir görüntü ikili seviyeye dönüştürüldükten sonra görüntü içerisindeki
  nesnenin konturunu çıkartılır.
- Kontur çıkartmak için ikili görüntü 1 piksel aşındırıldıktan sonra görüntünün
  aşındırılmamış ilk halinden bu yeni değeri çıkartılır. Böylece elimizde verilen
  görüntüye ait yalnızca nesneyi çevreleyen 1 piksel kalınlıkta bir çizgi (kontur) kalır.
- Yapılan işlem sonucu oluşan görüntüler aşağıdadır. Görüntü üzerinde 3x3 bir yapısal
  element kullanılarak 1 piksel genişlikte kontur elde edilmiştir.

<center><image src="./image/orn.jpg" width="400"></image></center>

## Açma

- Morfolojik açma işlemi, aşındırmayı takiben genişletme
  işleminin gerçekleştirilmesi işlemidir.
- Açma işleminde
  nesnelerin büyük çapta değişikliğe uğratılmadan ayrılması
  sağlanmaktadır.
- A işlenmesi amaçlanan görüntü matrisi
  B de yapısal eleman olsun.
- Bu durumda açma işlemiyle A
matrisindeki gereksiz kısımlar (küçük parçalar) görüntüdeki
nesneler zarar görmeden giderilmektedir.
<center><image src="./image/acma.jpg" width="400"></image></center>

## Kapama

- Kapama işlemi, açma işleminin tersine, genişletme işlemini
  takip eden aşındırma işleminin gerçekleştirilmesi işlemidir.
- Kapama işleminde birbirinden ayrı olan iki nesnenin
  büyük değişikliklere uğratılmadan birleştirilmesini
  sağlamaktır (görüntü içerisindeki ayrık parçalar birbirine
  yaklaşır).

<center><image src="./image/kapama.jpg" width="400"></image></center>

## İnceltme (Skeleton)

- İnceltme işlemi, verilen bir görüntüdeki nesnelerin
  yapısında ciddi bir değişiklik meydana getirmeden yapılan
  inceltme işlemidir.
- Nesnenin sınır piksellerinin
  değerlerine bağlı olarak nesnenin sınırlarının
  inceltilmesidir.
- Bir diğer adı da iskeletleştirmedir.

## Bağlı Parçalar (Connected Component)

- İkili formattaki bir görüntüde nesneler belirlendikten
  sonra birbirinden ayrılmayan parçalar 4-komşuluk veya 8-
  komşuluktan birine göre bağlı ise bağlı parçalar olarak
  nitelendirilmektedir.
- Bağlı parçalar genellikle elimine
  edilmek istenen bölgelerin belirli bir piksel sayısından
  düşük olması durumunda uygulanması kolaylık sağlayan
  bir yöntemdir.
- Bağlantılı bileşen etiketleme siyah-beyaz görüntüler üzerine
  uygulanan ve birbiri ile komşu olan piksellerin bir grup içerisinde
  toplamaya yarayan bir işlemdir.
- Bu gruplama sonucunda, resim üzerindeki her bir grup bir nesneyi
  temsil edecek şekilde numaralandırılır. Daha sonra da istenen grup
  numaralı nesne üzerinde kolaylıkla işlem yapılabilir.
- Bağlantılı bileşen etiketleme algoritması 4-komşuluk ve 8-komşuluk
  olarak ikiye ayrılır. Burada 8 komşuluk seçilirse çapraz piksellerin de
  komşu olduğu kabul edilmiş olur. Uygulamalarda genellikle 8-
  komşuluk tercih edilir
- Bağlantılı bileşen etiketleme için pek çok algoritma önerilse de
  sıklıkla kullanılan metot Two-Pass (Çift Geçiş)
  metodudur.
- Bu metotta ilk geçişte tüm pikseller tek tek gezilerek
  şu algoritma işletilir

- Piksel Siyaha Eşit Değilse

  - Pikselin Tüm komşularına (8 adet) bak - Tüm komşular siyah veya beyaz ise bu yeni bir pikseldir, piksele yeni bir etiket ata, diğer piksele geç - Komşulardan en az biri etiketli (siyah veya beyaz değil) ise piksele etiketli komşu / ların en küçük etiketlisini ata,
  <center><image src="./image/parcali.jpg" width="400"></image></center>

- Görüldüğü gibi ilk geçiş sonrası oluşan şekilde 1 ve 2 numaralı nesneler farklı
  nesnelermiş gibi görünseler de aslında bağlantılı (aynı) nesnelerdir.
- İkinci geçiş bunu önlemek için vardır.
- İkinci geçişte piksellere içerisindeki değerin gösterdiği değer yazılır.
- Mesela örneğimizde ikinci geçiş sonrası 2 etiketi
  görülen piksellere tabloya bakılarak (2->1) 1 etiketi yazılır.
- Böylece tüm bağımlı nesneler aynı etiket ile etiketlenmiş olur.

# GÖRÜNTÜ MORFLEME

- Morfleme kaynak görüntüyü hedef resme düzgün bir
  şekilde dönüştürecek görüntüler dizisi üretme tekniğidir.
- Bu teknik hareketli görüntülerde özel efektler
  oluşturmak için sıkça kullanılmaktadır.
- Düzgün bir dönüşüm elde etmek için öncelikle her iki
  görüntüdeki öznitelik noktaları aynı konuma gelecek
  şekilde görüntüler düzenlenir.
- Daha sonra düzenlenmiş görüntülerdeki renk değerleri
  görüntülere ait katsayılara göre birleştirilir.
- Morfleme tekniğinden görsel efektlerden başka ortalama yüzlerin
  elde edilmesinde, biyometride, animasyonlarda, birçok farklı
  amaç için faydalanılmaktadır (Wolberg 1990, Wolberg 2003, Lee
  2002, Beier 1992, Smithe 1990). Bu uygulamalarda 3 boyutlu
  yapının modellenmesi ile görünüş morfleme (Seitz 1996, Xiao
  2004), şekil morfleme (Alexa 2000, Yang 2009, Knag 2010), ifade
  morfleme (Fu 2004) ve harita morfleme (Reilly 2004, Nöllenburg 2008 gerçekleştirilmiştir. Diğer yandan ön-eğriltme (PreWarping)
  dönüşüm tekniği ile resimlerin bakış açısı
  değiştirilebilmektedir

- Morfleme, bir resmin diğer bir resme kademeli olarak
  dönüşümünü veya iki resmin çeşitli oranlarda birleştirilmesini
  ifade eder.
- Bir resmin diğerine dönüştürülmesi sırasında bu teknik, bir dizi
  görüntünün oluşmasını sağlar.
- Morfleme işlemi ilerledikçe birinci resim kaybolurken 2. resim
  görünmeye başlar. Bu nedenle oluşan görüntü dizisinin ilk
  yarısındaki görüntüler birinci resme, ikinci yarısındaki görüntüler
  ise ikinci resme daha çok benzemektedir.
- Görüntü dizisinin ortasındaki resim ise 1. ve 2. resmin
  ortalamasıdır

- Bir resmin diğer bir resme morfleme tekniği ile dönüştürülebilmesi
  için bazı kontrol noktalarının belirlenmesi gerekmektedir.
- Örneğin yüz görüntüleri için kontrol noktaları, yüzün
  şekillenmesinde belirleyici olan göz, kaş, burun, ağız vb.
  pozisyonlarıdır.
- Bu öznitelik noktaları kullanılarak görüntüler bölgelere
  parçalanmakta ve bu bölgeler üzerinde geometrik dönüşümler
  gerçekleştirilmektedir.
- Elde edilecek sonuç resminin kalitesi, alınan kontrol noktalarının
  sayısına bağlı olarak artmaktadır. Fakat nokta sayısının artışı bölge
  sayısını da artırdığından sistem performansını düşürecektir

- Örnekte, yüz görüntüleri üzerinde morfleme
  gerçekleştirilirken gözbebekleri (2), burun (1), ağız
  kenarları (2) ve yüz çevresini belirleyen 6 nokta olmak
  üzere toplam 11 kontrol noktası kullanılmaktadır. Bu
  noktalar kullanılarak yüz görüntüsü 14 üçgensel, 5
  dörtgensel bölgeye ayrılmıştır.
- Kaynak resimlerdeki kontrol noktalarının pozisyonları
  birbirinden farklı olduğu için, resimler arasında morfleme
  yapılırken, özellik noktalarını karışım yüzdesine göre aynı
  pozisyona getirmek amacıyla resimler eğritilmelidir
  (warping).
- Birbirine karşılık gelen üçgensel ve dörtgensel bölgelerin
  tanımlanmasından sonra, morfleme işlemi geometrik
  transformasyon problemine dönüşmektedir.
- Bu amaçla üçgensel ve dörtgensel bölgeler için sırasıyla
  afin ve bilineer dönüşümler kullanılmaktadır.

## Geometrik Dönüşümler

- Kontrol noktaları belirlenmiş ve bu noktalara bağlı olarak
bölgelere ayrılmış iki resim için ara bir resim üretmek için
resim ağırlıkları sırasıyla (alfa) ve (1-(alfa)) olarak belirlenir.
Birinci kaynak resimdeki A ve ikinci resimde bu noktaya
karşılık gelen B noktası ise, yeni özellik noktası F’yi
üretmek için lineer interpolasyon aşağıdaki gibidir.

  <center><image src="./image/geo.jpg" width="400"></image></center>

- Bu şekilde her iki kaynak resmin özellik noktalarının
  interpolasyonu ile üretilen yeni özellik noktaları resimleri
  orijinal bölgelerinden farklı bölgelere ayırmaktadır.
- Buradaki amaç her iki kaynak resmindeki orijinal bölgeleri
  bu yeni bölgelere dönüştürmektir.
- Böylece her iki kaynak resmi aynı bölgelere sahip
  olacaktır ve iki resmin (alfa) ve (1-(alfa)) ağırlıklarına göre
  birleştirilmesi mümkün hale gelecektir

# NESNE TANIMA

- Görüntü içinde belirli nesnelerin veya örüntülerin
  bulunması için birçok örüntü tanıma ve makine
  öğrenmesi yönteminden yararlanılır.
- Özellikle tıp, uzaktan algılama, savunma ve güvenlik gibi
  konular üzerinde karar verici sistem tasarımında nesne ve
  örüntü tanıma önemli bir uygulama alanını oluşturur.
- Bu bölümde örüntü tanıma ve makine öğrenmesi
  yöntemlerinin 2 boyutlu görüntülerde nasıl
  kullanılacağının aktarılması hedeflenmektedir.

## Nesne Tanımanın Temel Adımları

- Görüntü işleme açısından bir örüntü belli ortak
  özellikleri taşıyan, belli kurallara göre dizilime sahip piksel
  grupları olarak anlaşılabilir.
- Özellikle nesne tanımada, nesneye ait örüntülerin ortaya
  çıkarılması nesnenin konumunun tam olarak tespiti
  açısından önemlidir.
- Örüntülerin ve nesnelerin görüntü içinde tanınması için
  bazı temel matematiksel görüntü sunumlarının bilinmesi
  gerekir

## Görüntü Matrisleri

- İkili ve gri-seviye görüntüler basitçe 2-boyutlu bir matris
  yapısı şeklinde ifade edilebilirler.
- RGB, TIFF gibi renkli görüntüleri, birçok banttan oluşan,
  daha çok katmana sahip görüntüleri yüksek boyutlu (nboyutlu) görüntü matrisleri (veya görüntü küpü) olarak
  düşünebiliriz.

## Örüntü İfade Şekilleri

- Görüntülerden gerek uzamsal, gerek dönüşüm
  yöntemleri ile elde edilen elde edilen öznitelikler
  vektörler şeklinde ifade edilebilir.
- Vektörün uzunluğu olan d, aynı zamanda görüntüden
  elde edilen özniteliğin boyutu olarak adlandırılır.
- Tanımada direkt piksel değerleri kullanılacaksa öznitelik
  vektör boyutu d=genişlik x yükseklik olur

  <center><image src="./image/Nxdmatris.jpg" width="400"></image></center>

- N adet görüntüden elde edilen öznitelik matrisi
  (tanımada bu matris kullanılır- eğitim kümesi ve test kümesi ayrı
  ayrı olmalıdır, eğitim kümesi ile sistem eğitilir, test kümesi ile
  eğitilen sistemin tanıma performansı değerlendirilir.)

## Nesne ve Örüntü Tanıma İşleminin Bileşenleri

- Temel olarak kamera ve algılayıcılar vasıtasıyla elde edilen
  görüntüde ilgili nesne ve örüntülerin tanınabilmesi için
  genel bir şablon olarak izlenmesi gereken basamaklar
  şunlardır:
  - Ön İşleme
  - Özellik Seçimi veya Çıkarımı
  - Eğiticili (supervised) sınıflandırma veya eğiticisiz (unsupervised)
    kümele yöntemleri kullanarak model altyapısının kurulumu
  - Son İşleme

## Ön İşleme

- Nesne veya örüntü tanıma algoritmalarının daha başarılı olabilmesi için
  görüntülerde bir takım ön işlemlerin yapılması gerekebilir.
- Gürültü Giderimi: Görüntüdeki gürültünün varlığı oluşturulacak modelin
  sağlamlığını ve kullanacak sınıflandırma ve kümeleme algoritmalarının başarımını
  olumsuz olarak etkiler.
- Süzgeçleme: Gerek görüntülerde gürültü giderimi, yumuşatma, keskinleştirme,
  kenar çıkarımı için süzgeçlemeden yararlanılır.
- Normalizasyon: Kullanılan algoritmalar belirli değer aralıklarında daha iyi sonuçlar
  üretir. Bu yüzden özellik olarak kullanılan parlaklık, renk gibi değerlerin standart
  sapması ve ortalaması gibi değerler kullanarak veya en büyük özellik değeri 1
  olacak şekilde bölme yaparak farklı normalizasyon işlemleri gerçekleştirilir.
  Örneğin standart skor normalizasyonunda ortalama ve standart sapma gibi
  değerler kullanılır:
- Aykırı Değer Giderimi: Veri yapısında bulunmaması gereken algılayıcı hatasına veya
  kayıt hatasına dayanan bütünlüğü bozan verilerin ayrıştırılması işlemidir.

## Öznitelik Seçimi ve Çıkarımı

- Ele alınan görüntü verisinden gerekli ayrıştırıcı özniteliklerin
  çıkarılması önemli bir işlem adımıdır.
- Özellik seçimi ve çıkarımında verinin ayrıştırıcılığını kaybetmeden
  veya mümkünse arttırarak olabildiğince az sayıda öznitelik
  kullanılarak sınıflandırma ve kümeleme başarımının arttırılması
  hedeflenir.
- Özniteliklerin seçilmesi için var olan parlaklık, renk gibi değerler
  kümesinden seçilmiş alt bir küme kullanılabileceği gibi dönüşüm
  yöntemleri de kullanılabilir.
- Özellik çıkarımında dönüşüm yöntemlerinin yansıra, uzamsal yapıdan
  da yararlanarak çeşitli istatistiksel öznitelikler çıkarılabilir.

## Öznitelik Seçimi ve Çıkarımı

- Özellik çıkarımı ve boyut indirgeme yöntemleri birbiri ile oldukça
  alakalıdır.
- Birçok yüksek boyutlu sınıflama ve kümeleme probleminde olduğu
  gibi görüntüye ait verilerde de kullanılan klasik örüntü tanıma
  algoritmalarını olumsuz yönde etkilemektedir.
- Ayrıca eğitim örneklerinin (etiket bilgisi olan örneklerin) sabit
  olduğu durumlarda boyut arttıkça ayrıştırıcılık gücünün azaldığı
  gözlemlenir.
- Bu problemin üstesinden gelebilmek için birçok doğrusal veya
  doğrusal olmayan boyut indirgeme yönteminden yararlanılmaktadır.
- Bunun nedeni, boyut indirgeme algoritmalarında veriyi en iyi temsil
  eden özelliklerin çıkarılarak örüntü tanıma ve makine öğrenmesi
  algoritmalarında kullanılmasıdır.

## Boyut İndirgeme Yöntemleri

- Boyut indirgeme yöntemlerini doğrusal ve doğrusal olmayan
  yöntemler olmak üzere iki temel başlıkta inceleyebiliriz.
- Doğrusal yöntemler veri içindeki doğrusal olarak ifade
  edilebilen verileri düşük boyutlarda ifade edilebilirken
  doğrusal olmayan yöntemler veri içerisinde doğrusal olarak
  ayrıştırılamayan verileri daha düşük boyutlarda ifade
  edebilme imkânına sahiptir.

  <center><image src="./image/Nxdmatris1.jpg" width="400"></image></center>

## Doğrusal Boyut İndirgeme Yöntemleri

- Temel Bileşen Analizi (Principal Component Analysis)
- Doğrusal Ayrıştırıcı Analizi (Linear Discriminant Analysis)
- Bağımsız Bileşen Analizi (Independent Component
  Analysis)
- Negatif Olmayan Matris Ayrıştırması (Non-negative
  matrix factorization)

## Doğrusal Olmayan Boyut İndirgemeYöntemleri

- Bölgesel özellikleri koruyan yöntemler:
  - Bölgesel Doğrusal Gömü (Local Linear Embedding)
  - Laplas Özharitalar (Laplacian Eigenmaps)
  - Hessian LLE
  - Doğrusal Tanjant Uzay Analizi (LinearTangent Space Analysis)
- Küresel özellikleri koruyan yöntemler:
  - Çok Boyutlu Ölçekleme (Multidimensional Scaling)
  - Isomap
  - Çekirdek Temel Bileşen Analizi (Kernel PCA)
  - Çekirdek Doğrusal Ayrıştırıcı Analizi (Kernel LDA)
  - Yayılma Haritaları (Diffusion Maps)

## Eğiticisiz Öğrenme Yöntemler

- Eğiticisiz öğrenme yöntemleri etiket bilgileri olmaksızın
  (verinin ne olduğunu bilmeksizin) veride gizli bulunan
  yapıyı ortaya çıkarmaya çalışır.
- Eğiticisiz öğrenmede etiket
  bilgileri olmadığı için veri içindeki gruplaşmalar/ grup
  yapıları ne kadar iyi temsil edilirse öğrenme o kadar
  başarılı olur.
- Birçok kümeleme yöntemi verilerin eğiticisiz
  biçimde temsil edilebilmesi için kullanılmaktadır.
- Bu yöntemler şu alt sınıflara ayrıştırılabilir:

## Hiyerarşik Kümeleme

- Hiyerarşik kümelemede veri noktalarının birbirine olan
  uzaklığına göre iç gruplaşmalar ortaya çıkarılmaya çalışılır.
- Birbirine yakın/uzak olan noktalar dendrogramlar (öbek
  ağaçları) vasıtasıyla çeşitli yakınlık/benzerlik ölçütleri esas
  alınıp, ayrıştırılarak veya birleştirilerek hiyerarşik
  kümeleme gerçekleştirilir
- Bu tür kümelemede sıkça kullanılan iki yöntem ise
  - Tek-bağlantılı kümeleme (Single-linkage)
  - Tüm-bağlantılı kümeleme’dir (Complete-linkage).

## Veri Dağılımını Esas Alan Kümeleme

- Veri dağılımını esas alan yöntemlerde istatistiksel dağılım
  modellerinden yararlanılır.
- Temel amaç çok boyutlu veri
  içerisindeki kümelerin en uygun dağılım şeklini veren
  dağılım parametrelerinin belirlenmesidir.
- Gauss Karışım
  Modellerine dayanan (Gaussian Mixture Models), beklenti
  en-büyüklenmesi (Expectation Maximization) yöntemi en
  bilindik yaklaşımdır.
- Bu yöntemde kümelerin verideki
  optimum dağılım uyumluluğu Gauss dağılımı esas alınarak
  sağlanmaya çalışılır.

## Ağırlık Merkezi Tabanlı Yöntemler

- Ağırlık merkezi tabanlı yöntemlerde öncelikli olarak
  bulunması istenen küme sayısının algoritmaya giriş olarak
  verilmesi gerekir.
- Verilen küme sayısınca başlangıç noktaları
  rastgele veya önceden belirlenerek uzaklık hesabına göre
  kümeleme gerçekleştirilir.
- Kümeleme sonuçları kesin (hard)
  olabileceği gibi bulanık (fuzzy) olarak da belirlenebilir.
- En bilinen yöntem olan k-ortalamalar algoritmasında kümeleme
  sonucu kesin olarak belirlenirken, bulanık c-ortalamalar
  algoritmasında sonuçlar bulanık olarak (değişik kümelere
  aidiyet dereceleri verilerek) kümeleme gerçekleştirilir.

## İstatistiksel Veri Yoğunluğuna Dayalı Yöntemler

- Veriyi oluşturan noktaların çok boyutlu uzayda yoğunlaştığı
  yerleri bulmayı amaçlayan bu yöntem veri yoğunluğuna dayalı
  yöntemler olarak adlandırılırlar.
- Kümeler arasındaki sınır
  geçişlerinde veri yoğunluğunun azaldığı varsayılarak küme
  sınırları belirlenir.
- En sık kullanılan yöntemler ise
  - DBSCAN (Density-based spatial clustering of applications with
    noise)
  - OPTICS (Ordering points to identify the clustering structure)’dir.

## Yapay Sinir Ağlarına Dayalı Kümeleme

- Ayrıca yapay sinir ağları kapsamında ele alınabilecek
  kümeleme yönteleri ise
  - Öz-düzenlemeli Haritalar (Self Organizing Maps)
  - Uyarlamalı Rezonans Teorisi (Adaptive ResonanceTheory)’dir.

## Eğiticili Öğrenme Yöntemleri

- Eğiticili öğrenme yöntemlerinde, eğiticisiz yöntemlerden farklı olarak
  etiketli veriden yararlanılarak model oluşturulmaya çalışılır.
- Öncelikle olarak modelin oluşturulması için bir ‘eğitim kümesinden’ yararlanılır.
- Eğitim kümesi aslında verinin yapısını özetleyebilecek olan bir alt kümedir.
- Oluşturulacak olan modelin en uygun şekilde ayarlanabilmesi için
  parametre optimizasyonu eğitim kümesi kullanılarak gerçekleştirilir.
- Daha sonra ‘test’ ve ‘geçerlilik’ kümeleri kullanılarak modelin verimliliği test
  edilmiş olur.
- En çok kullanılan eğiticili öğrenme yöntemleri ise ana
  başlıklar halinde şu şekilde verilebilir
  - Bayes Sınıflayıcıları
  - K-EnYakın Komşuluk
  - Yapay Sinir Ağları
  - DestekVektör Makineler
- Başka bir başlık altında ise karışım modelleri ve topluluk sınıflayıcıları da
  eğiticili öğrenme yöntemleri olarak incelenebilir.

## Takviyeli Öğrenme Yöntemleri

- Eğiticili öğrenme yöntemlerinden farklı olarak, eğitim
  modeli oluşturulurken her adımda etiket bilgileri sağlayan
  bir eğitici olmaması durumunda sistem, ödül ve ceza
  kavramlarında yararlanılarak istenilen modeli en başarılı
  biçimde oluşturmaya çalışır.
- Psikolojideki ödül ve ceza
  kavramları ile ilişkilendirilerek eğitim modeli optimal bir
  biçimde algoritmik olarak oluşturulur.

## Son İşleme

- Elde edilen sınıflandırma veya kümeleme sonuçlarının
  iyileştirilmesi için yapılan her türlü işlem son işleme
  başlığı altında işlenebilir.
- Son işlemede görüntüdeki
  uzamsal ilişkilerden yararlanılarak atanmış olan etiket
  bilgileri tekrar değerlendirilebileceği gibi biçim-bilimsel
  işlemciler kullanılarak sınıflama veya kümeleme
  başarımının artırılması amaçlanır
