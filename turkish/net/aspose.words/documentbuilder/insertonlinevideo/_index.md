---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: .NET için Aspose.Words
description: Gelişmiş etkileşim ve yaratıcılık için DocumentBuilder'ın InsertOnlineVideo yöntemiyle belgelerinize çevrimiçi videoları zahmetsizce ekleyin ve ölçeklendirin.
type: docs
weight: 440
url: /tr/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Görüntünün başlangıç noktasından sol tarafa kadar olan mesafe. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Görüntünün başlangıç noktasından üst tarafına kadar olan mesafenin nokta cinsinden ifadesi. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| wrapType | WrapType | Metnin resmin etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

Aşağıdaki kaynaklardan çevrimiçi video eklenmesi desteklenmektedir:

* https://www.youtube.com/
* https://vimeo.com/

Çevrimiçi videonuz düzgün görüntülenmiyorsa, şunu kullanın:`InsertOnlineVideo`, özel gömülü html kodunu kabul eder.

Video yerleştirme kodu sağlayıcılar arasında farklılık gösterebilir, ayrıntılar için ilgili sağlayıcınıza danışın.

## Örnekler

Çevrimiçi bir videonun bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Microsoft Word'de tıklandığında web'den bir video oynatan bir şekil ekleyin.
// Bu dikdörtgen şekil, bağlantılı videonun ilk karesine dayalı bir görüntü içerecektir
// ve bir "oynat düğmesi" görsel istemi. Videonun en boy oranı 16:9'dur.
// Şeklin boyutunu bu orana ayarlayacağız, böylece görüntü gerilmiş görünmeyecek.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| videoEmbedCode | String | Videonun yerleştirme kodu. |
| thumbnailImageBytes | Byte[] | Küçük resim görüntü baytları. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Özel küçük resimle bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" genişlik=\"640\" yükseklik=\"360\" çerçevekenarlığı=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Aşağıda, çevrimiçi bir videoya bağlantı veren özel bir küçük resimle bir şekil oluşturmanın iki yolu bulunmaktadır
        // Microsoft Word'de şekle tıkladığımızda çalacak.
        // 1 - Oluşturucunun düğüm ekleme imlecine satır içi bir şekil ekle:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Yüzen bir şekil ekle:
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| videoEmbedCode | String | Videonun yerleştirme kodu. |
| thumbnailImageBytes | Byte[] | Küçük resim görüntü baytları. |
| horzPos | RelativeHorizontalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| left | Double | Görüntünün başlangıç noktasından sol tarafa kadar olan mesafe. |
| vertPos | RelativeVerticalPosition | Görüntüye olan mesafenin nereden ölçüleceğini belirtir. |
| top | Double | Görüntünün başlangıç noktasından üst tarafına kadar olan mesafenin nokta cinsinden ifadesi. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| wrapType | WrapType | Metnin resmin etrafına nasıl sarılacağını belirtir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Özel küçük resimle bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" genişlik=\"640\" yükseklik=\"360\" çerçevekenarlığı=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // Aşağıda, çevrimiçi bir videoya bağlantı veren özel bir küçük resimle bir şekil oluşturmanın iki yolu bulunmaktadır
        // Microsoft Word'de şekle tıkladığımızda çalacak.
        // 1 - Oluşturucunun düğüm ekleme imlecine satır içi bir şekil ekle:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Yüzen bir şekil ekle:
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| videoUrl | String | Videonun URL'si. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

Aşağıdaki kaynaklardan çevrimiçi video eklenmesi desteklenmektedir:

* https://www.youtube.com/
* https://vimeo.com/

Çevrimiçi videonuz düzgün görüntülenmiyorsa, şunu kullanın:`InsertOnlineVideo`, özel gömülü html kodunu kabul eder.

Video yerleştirme kodu sağlayıcılar arasında farklılık gösterebilir, ayrıntılar için ilgili sağlayıcınıza danışın.

## Örnekler

Bir URL kullanarak bir belgeye çevrimiçi videonun nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360, 270);

// Şeklin üzerine tıklayarak Microsoft Word'den videoyu izleyebiliriz.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
