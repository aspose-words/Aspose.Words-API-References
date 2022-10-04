---
title: InsertOnlineVideo
second_title: Aspose.Words for .NET API Referansı
description: Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir.
type: docs
weight: 390
url: /tr/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

öğesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

Aşağıdaki kaynaklardan çevrimiçi video eklenmesi desteklenir:

* https://www.youtube.com/
* https://vimeo.com/

Çevrimiçi videonuz düzgün görüntülenmiyorsa, şunu kullanın:[`InsertOnlineVideo`](./insertonlinevideo/), özel gömülü html kodunu kabul eder.

Video yerleştirme kodu sağlayıcılar arasında değişiklik gösterebilir, ayrıntılar için ilgili sağlayıcınıza danışın.

### Örnekler

URL kullanarak bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Şekle tıklayarak videoyu Microsoft Word'den izleyebiliriz.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan uzaklığın nereden ölçüldüğünü belirtir. |
| left | Double | Görüntünün başlangıç noktasından sol tarafına nokta cinsinden uzaklık. |
| vertPos | RelativeVerticalPosition | Görüntüye olan uzaklığın nereden ölçüleceğini belirtir. |
| top | Double | Görüntünün başlangıç noktasından üst tarafına nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |
| wrapType | WrapType | Metnin görüntünün etrafına nasıl kaydırılacağını belirtir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

öğesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

Aşağıdaki kaynaklardan çevrimiçi video eklenmesi desteklenir:

* https://www.youtube.com/
* https://vimeo.com/

Çevrimiçi videonuz düzgün görüntülenmiyorsa, şunu kullanın:[`InsertOnlineVideo`](./insertonlinevideo/), özel gömülü html kodunu kabul eder.

Video yerleştirme kodu sağlayıcılar arasında değişiklik gösterebilir, ayrıntılar için ilgili sağlayıcınıza danışın.

### Örnekler

Bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Microsoft Word'de tıklandığında web'den video oynatan bir şekil ekleyin.
// Bu dikdörtgen şekil, bağlantılı videonun ilk karesine dayalı bir resim içerecektir
// ve bir "oynat düğmesi" görsel istemi. Videonun en boy oranı 16:9.
// Şeklin boyutunu bu orana göre ayarlayacağız, böylece görüntü gergin görünmez.
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

Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| videoEmbedCode | String | Videonun gömme kodu. |
| thumbnailImageBytes | Byte[] | Küçük resim baytları. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

öğesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Özel bir küçük resimle çevrimiçi bir videonun bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Aşağıda, çevrimiçi bir videoya bağlantı veren özel bir küçük resim ile bir şekil oluşturmanın iki yolu bulunmaktadır.
        // Microsoft Word'deki şekle tıkladığımızda oynayacak.
        // 1 - Oluşturucunun düğüm ekleme imlecine bir satır içi şekil ekleyin:
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

Belgeye çevrimiçi bir video nesnesi ekler ve onu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| videoEmbedCode | String | Videonun gömme kodu. |
| thumbnailImageBytes | Byte[] | Küçük resim baytları. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan uzaklığın nereden ölçüldüğünü belirtir. |
| left | Double | Görüntünün başlangıç noktasından sol tarafına nokta cinsinden uzaklık. |
| vertPos | RelativeVerticalPosition | Görüntüye olan uzaklığın nereden ölçüleceğini belirtir. |
| top | Double | Görüntünün başlangıç noktasından üst tarafına nokta cinsinden uzaklık. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değeri olabilir. |
| wrapType | WrapType | Metnin görüntünün etrafına nasıl kaydırılacağını belirtir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

öğesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Özel bir küçük resimle çevrimiçi bir videonun bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Aşağıda, çevrimiçi bir videoya bağlantı veren özel bir küçük resim ile bir şekil oluşturmanın iki yolu bulunmaktadır.
        // Microsoft Word'deki şekle tıkladığımızda oynayacak.
        // 1 - Oluşturucunun düğüm ekleme imlecine bir satır içi şekil ekleyin:
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
