---
title: DocumentBuilder.InsertImage
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. .NETten bir görüntü eklerImage nesnesini belgeye ekleyin. Resim satır içi ve 100 ölçekte eklenir.
type: docs
weight: 380
url: /tr/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

.NET'ten bir görüntü eklerImage nesnesini belgeye ekleyin. Resim satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(Image image)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Belgeye eklenecek resim. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Bir nesneden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Aşağıda bir Image nesne örneğinden bir görsel eklemenin üç yolu verilmiştir.
// 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip kayan şekil:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(string) {#insertimage_9}

Bir dosyadan veya URL'den belgeye bir resim ekler. Resim satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resmin bulunduğu dosya. Geçerli herhangi bir yerel veya uzak URI olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

Bu aşırı yükleme, uzak bir URI belirtirseniz, document dosyasına eklenmeden önce görüntüyü otomatik olarak indirecektir.

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Belgeye gif görüntüsünün nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Yol veya bayt dizisini kullanarak gif resmi ekleyebiliriz.
// Yalnızca DocumentBuilder'ın Word 2010 veya daha yüksek bir sürüme göre optimize edilmesi durumunda çalışır.
// Görüntü baytlarına erişimin Gif'in Png'ye dönüştürülmesine neden olduğunu unutmayın.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Görüntü içeren bir şeklin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda belge oluşturucunun "InsertShape" yönteminin bulunduğu iki konum bulunmaktadır
// şeklin görüntüleyeceği görüntüyü kaynaklayabiliriz.
// 1 - Bir görüntü dosyasının yerel dosya sistemi dosya adını iletin:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Bir resme işaret eden bir URL iletin.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Çakışan metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Hangi görüntünün ekleneceğinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words, SVG görüntüsünü svgBlip uzantılı PNG olarak belgeye ekler
// orijinal vektör SVG görüntü temsilini içerir.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words, Microsoft Word'ün eski formatta yaptığı gibi SVG görüntüsünü belgeye PNG olarak ekler.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words, görüntüyü vektör temsilinde tutmak için SVG görüntüsünü belgeye EMF meta dosyası olarak ekler.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Yerel dosya sisteminden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel sistem dosya adından resim eklemenin üç yolu verilmiştir.
// 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip kayan şekil:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(Stream) {#insertimage_6}

Bir akıştan belgeye bir görüntü ekler. Resim satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Resmi içeren akış. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Akıştaki görüntü içeren bir şeklin belgeye nasıl ekleneceğini gösterir.

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

Bir akıştan bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir akıştan resim eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(byte[]) {#insertimage}

Bayt dizisinden belgeye bir görüntü ekler. Resim satır içi ve %100 ölçekte eklenir.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Görüntüyü içeren bayt dizisi. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Bayt dizisinden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Aşağıda bayt dizisinden resim eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Bayt dizisinden bir görüntünün bir belgeye nasıl ekleneceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntünün kodunun çözülmesi onu .png formatına dönüştürecektir.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Aşağıda bayt dizisinden resim eklemenin üç yolu verilmiştir.
            // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Özel boyutlara sahip satır içi şekil:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Özel boyutlara sahip kayan şekil:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(Image, double, double) {#insertimage_5}

.NET'ten satır içi görüntü eklerImage nesnesini belgeye ekler ve onu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Belgeye eklenecek resim. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Bir nesneden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Aşağıda bir Image nesne örneğinden bir görsel eklemenin üç yolu verilmiştir.
// 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip kayan şekil:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Bir nesneden bir görüntünün belgeye nasıl ekleneceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntünün kodunun çözülmesi onu .png formatına dönüştürecektir.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir Image nesne örneğinden bir görsel eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(string, double, double) {#insertimage_11}

Bir dosyadan veya URL'den belgeye satır içi bir resim ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resmin bulunduğu dosya. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Yerel dosya sisteminden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel sistem dosya adından resim eklemenin üç yolu verilmiştir.
// 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip kayan şekil:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(Stream, double, double) {#insertimage_8}

Bir akıştan belgeye satır içi bir görüntü ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Görüntüyü içeren akış. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Bir akıştan bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir akıştan resim eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(byte[], double, double) {#insertimage_2}

Bayt dizisinden satır içi bir görüntüyü belgeye ekler ve bunu belirtilen boyuta ölçeklendirir.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Görüntüyü içeren bayt dizisi. |
| width | Double | Nokta cinsinden görüntünün genişliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |
| height | Double | Nokta cinsinden görüntünün yüksekliği. %100 ölçek istemek için negatif veya sıfır değer olabilir. |

### Geri dönüş değeri

Yeni eklenen görüntü düğümü.

### Notlar

'yi kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.[`Shape`](../../../aspose.words.drawing/shape/) Bu yöntemle döndürülen nesne.

### Örnekler

Bayt dizisinden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Aşağıda bayt dizisinden resim eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Bayt dizisinden bir görüntünün bir belgeye nasıl ekleneceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntünün kodunun çözülmesi onu .png formatına dönüştürecektir.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Aşağıda bayt dizisinden resim eklemenin üç yolu verilmiştir.
            // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Özel boyutlara sahip satır içi şekil:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Özel boyutlara sahip kayan şekil:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_4}

.NET'ten bir görüntü eklerImage belirtilen konum ve boyuttaki nesne.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Belgeye eklenecek resim. |
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

Bir nesneden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// Aşağıda bir Image nesne örneğinden bir görsel eklemenin üç yolu verilmiştir.
// 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip kayan şekil:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Bir nesneden bir görüntünün belgeye nasıl ekleneceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntünün kodunun çözülmesi onu .png formatına dönüştürecektir.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir Image nesne örneğinden bir görsel eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
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

## InsertImage(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_10}

Bir dosyadan veya URL'den belirtilen konuma ve boyuta bir resim ekler.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Resmin bulunduğu dosya. |
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

Bir resmin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir görüntüyü kaynaklamak ve ardından onu kayan bir şekil olarak eklemek için belge oluşturucuyu kullanmanın iki yolu vardır.
// 1 - Yerel dosya sistemindeki bir dosyadan:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Bir URL'den:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Yerel dosya sisteminden bir görüntünün boyutlarını koruyarak belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// InsertImage yöntemi, görüntü verilerinde iletilen görüntüyle birlikte kayan bir şekil oluşturur.
// Şeklin boyutlarını bu yönteme geçirerek belirtebiliriz.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// İstenilen boyutlar olarak negatif değerlerin iletilmesi otomatik olarak tanımlanacaktır
// şeklin boyutları, görüntünün boyutlarına göre belirlenir.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Yerel dosya sisteminden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda yerel sistem dosya adından resim eklemenin üç yolu verilmiştir.
// 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Özel boyutlara sahip satır içi şekil:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Özel boyutlara sahip kayan şekil:
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
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_7}

Belirtilen konum ve boyutta bir akıştan bir görüntü ekler.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Görüntüyü içeren akış. |
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

Bir akıştan bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Aşağıda bir akıştan resim eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
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
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertImage(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_1}

Belirtilen konum ve boyutta bir bayt dizisinden bir görüntü ekler.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageBytes | Byte[] | Görüntüyü içeren bayt dizisi. |
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

Bayt dizisinden bir görüntünün belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // Aşağıda bayt dizisinden resim eklemenin üç yolu verilmiştir.
    // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Özel boyutlara sahip satır içi şekil:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Özel boyutlara sahip kayan şekil:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Bayt dizisinden bir görüntünün bir belgeye nasıl ekleneceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Görüntünün kodunun çözülmesi onu .png formatına dönüştürecektir.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // Aşağıda bayt dizisinden resim eklemenin üç yolu verilmiştir.
            // 1 - Görüntünün orijinal boyutlarına göre varsayılan boyuta sahip satır içi şekil:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Özel boyutlara sahip satır içi şekil:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Özel boyutlara sahip kayan şekil:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


