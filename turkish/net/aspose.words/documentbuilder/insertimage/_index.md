---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: .NET için Aspose.Words
description: DocumentBuilder'ın InsertImage yöntemiyle belgelerinizi zahmetsizce geliştirin ve çarpıcı görseller için .NET görüntülerinin tam ölçekte sorunsuz bir şekilde eklenmesini sağlayın.
type: docs
weight: 400
url: /tr/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

.NET'ten bir görüntü eklerImage nesnesini belgeye ekleyin. Görüntü satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(Image image)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Belgeye eklenecek resim. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir nesneden bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Aşağıda Image nesnesi örneğinden bir resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

Bir dosyadan veya URL'den belgeye bir resim ekler. Resim satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Görüntünün bulunduğu dosya. Herhangi bir geçerli yerel veya uzak URI olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

Uzak bir URI belirtirseniz, bu aşırı yükleme document 'ye eklemeden önce görüntüyü otomatik olarak indirecektir.

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

WebP resminin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "WebP image.webp");

doc.Save(ArtifactsDir + "Image.InsertWebpImage.docx");
```

Belgeye gif resminin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Yol veya bayt dizisi kullanarak gif resmi ekleyebiliriz.
// Bu yalnızca DocumentBuilder'ın Word 2010 veya üzeri sürümlere optimize edilmesi durumunda çalışır.
// Resim baytlarına erişimin Gif'i PNG'ye dönüştürdüğünü unutmayın.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Bir belgeye resimli bir şeklin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, belge oluşturucunun "InsertShape" yönteminin kullanıldığı iki konum bulunmaktadır
// şeklin göstereceği görseli kaynak olarak kullanabiliriz.
// 1 - Bir görüntü dosyasının yerel dosya sistemi dosya adını geçirin:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Bir resme işaret eden bir URL geçirin.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Sayfanın ortasına kayan bir resmin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste gelen metnin arkasında görünecek yüzen bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Hangi resmin ekleneceğini nasıl belirleyeceğinizi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words, SVG resmini svgBlip uzantısıyla PNG olarak belgeye ekler
// orijinal vektör SVG görüntü gösterimini içerir.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words, Microsoft Word'ün eski formatlarda yaptığı gibi, SVG resmini PNG olarak belgeye ekler.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words, görüntünün vektörel gösterimini korumak için SVG görüntüsünü EMF meta dosyası olarak belgeye ekler.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Yerel dosya sisteminden bir resmin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel sistem dosya adından bir resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

Bir akıştan belgeye bir görüntü ekler. Görüntü satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Görüntüyü içeren akış. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir akıştan bir resim içeren bir şeklin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Bir akıştan bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir akıştan resim eklemenin üç yolu bulunmaktadır.
    // 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip yüzen şekil:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

Bir bayt dizisinden belgeye bir görüntü ekler. Görüntü satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Resmi içeren bayt dizisi. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir bayt dizisinden bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Aşağıda bir bayt dizisinden resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

.NET'ten satır içi bir resim eklerImage nesnesini belgeye ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Belgeye eklenecek resim. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir nesneden bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Aşağıda Image nesnesi örneğinden bir resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

Bir dosyadan veya URL'den belgeye satır içi bir resim ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resmin bulunduğu dosya. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Yerel dosya sisteminden bir resmin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel sistem dosya adından bir resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

Bir akıştan belgeye satır içi bir resim ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Resmin bulunduğu akış. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir akıştan bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir akıştan resim eklemenin üç yolu bulunmaktadır.
    // 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip yüzen şekil:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

Bir bayt dizisinden belgeye satır içi bir resim ekler ve belirtilen boyuta ölçekler.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Resmi içeren bayt dizisi. |
| width | Double | Resmin noktalardaki genişliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |
| height | Double | Resmin nokta cinsinden yüksekliği. %100 ölçek talep etmek için negatif veya sıfır değeri olabilir. |

### Geri dönüş değeri

Az önce eklenen görüntü düğümü.

## Notlar

kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu metot tarafından döndürülen nesne.

## Örnekler

Bir bayt dizisinden bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Aşağıda bir bayt dizisinden resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

.NET'ten bir görüntü eklerImage Belirtilen konum ve boyutta nesnesi.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Belgeye eklenecek resim. |
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

Bir nesneden bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Aşağıda Image nesnesi örneğinden bir resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
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

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

Belirtilen konuma ve boyuta bir dosyadan veya URL'den bir resim ekler.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resmin bulunduğu dosya. |
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

Resim eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir belge oluşturucuyu kullanarak bir görüntüyü kaynaklamanın ve ardından onu yüzen bir şekil olarak eklemenin iki yolu vardır.
// 1 - Yerel dosya sistemindeki bir dosyadan:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Bir URL'den:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Yerel dosya sisteminden bir görüntünün boyutlarını koruyarak bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// InsertImage yöntemi, resim verilerinde geçirilen resimle yüzen bir şekil oluşturur.
// Şeklin boyutlarını bu metoda geçirerek belirleyebiliriz.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Amaçlanan boyutlar olarak negatif değerlerin geçirilmesi otomatik olarak tanımlanacaktır
// şeklin boyutları, resminin boyutlarına göre belirlenir.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Yerel dosya sisteminden bir resmin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel sistem dosya adından bir resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
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

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

Belirtilen konum ve boyutta bir akıştan bir görüntü ekler.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Resmin bulunduğu akış. |
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

Bir akıştan bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir akıştan resim eklemenin üç yolu bulunmaktadır.
    // 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip yüzen şekil:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
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

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

Belirtilen konum ve boyutta bir bayt dizisinden bir resim ekler.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Resmi içeren bayt dizisi. |
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

Bir bayt dizisinden bir belgeye nasıl resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Aşağıda bir bayt dizisinden resim eklemenin üç yolu bulunmaktadır.
// 1 - Resmin orijinal boyutlarına dayalı varsayılan bir boyuta sahip satır içi şekil:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip yüzen şekil:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
