---
title: DocumentBuilder.InsertOnlineVideo
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.
type: docs
weight: 420
url: /tr/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

Aşağıdaki kaynaklardan çevrimiçi video eklenmesi desteklenir:

* https://www.youtube.com/
* https://vimeo.com/

Çevrimiçi videonuz doğru şekilde görüntülenmiyorsa şunu kullanın:`InsertOnlineVideo`, özel gömülü html kodunu kabul eder.

Video yerleştirme kodu sağlayıcılar arasında değişiklik gösterebilir; ayrıntılar için ilgili sağlayıcınıza danışın.

### Örnekler

URL kullanarak çevrimiçi bir videonun bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Şeklin üzerine tıklayarak Microsoft Word'den videoyu izleyebiliriz.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Nokta cinsinden görüntünün başlangıç noktasından sol tarafına olan uzaklık. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüldüğünü belirtir. |
| top | Double | Orijinden görüntünün üst kısmına kadar olan nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| wrapType | WrapType | Metnin görüntünün etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

Aşağıdaki kaynaklardan çevrimiçi video eklenmesi desteklenir:

* https://www.youtube.com/
* https://vimeo.com/

Çevrimiçi videonuz doğru şekilde görüntülenmiyorsa şunu kullanın:`InsertOnlineVideo`, özel gömülü html kodunu kabul eder.

Video yerleştirme kodu sağlayıcılar arasında değişiklik gösterebilir; ayrıntılar için ilgili sağlayıcınıza danışın.

### Örnekler

Çevrimiçi videonun bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Microsoft Word'de tıklandığında web'den video oynatan bir şekil ekleyin.
// Bu dikdörtgen şekil, bağlantılı videonun ilk karesine dayalı bir görüntü içerecektir
// ve bir "oynat düğmesi" görsel istemi. Videonun en boy oranı 16:9'dur.
// Şeklin boyutunu bu orana ayarlayacağız, böylece görüntü gergin görünmüyor.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| videoEmbedCode | String | Videonun yerleştirme kodu. |
| thumbnailImageBytes | Byte[] | Küçük resim görüntüsü baytları. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Özel küçük resim içeren bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" genişlik=\"640\" yükseklik=\"360\" çerçeveborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Aşağıda, çevrimiçi bir videoya bağlantı veren özel küçük resimle şekil oluşturmanın iki yolu verilmiştir
        // Microsoft Word'deki şekle tıkladığımızda çalacak.
        // 1 - Oluşturucunun düğüm ekleme imlecine satır içi bir şekil ekleyin:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Kayan bir şekil ekleyin:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

Belgeye bir çevrimiçi video nesnesi ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| videoEmbedCode | String | Videonun yerleştirme kodu. |
| thumbnailImageBytes | Byte[] | Küçük resim görüntüsü baytları. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Nokta cinsinden görüntünün başlangıç noktasından sol tarafına olan uzaklık. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüldüğünü belirtir. |
| top | Double | Orijinden görüntünün üst kısmına kadar olan nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| wrapType | WrapType | Metnin görüntünün etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Özel küçük resim içeren bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" genişlik=\"640\" yükseklik=\"360\" çerçeveborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Aşağıda, çevrimiçi bir videoya bağlantı veren özel küçük resimle şekil oluşturmanın iki yolu verilmiştir
        // Microsoft Word'deki şekle tıkladığımızda çalacak.
        // 1 - Oluşturucunun düğüm ekleme imlecine satır içi bir şekil ekleyin:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Kayan bir şekil ekleyin:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


