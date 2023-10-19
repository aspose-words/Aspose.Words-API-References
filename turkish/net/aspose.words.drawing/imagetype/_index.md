---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ImageType Sıralama. Microsoft Word belgesindeki görüntünün türünü biçimini belirtir C#'da.
type: docs
weight: 1080
url: /tr/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Microsoft Word belgesindeki görüntünün türünü (biçimini) belirtir.

```csharp
public enum ImageType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| NoImage | `0` | Resim verisi yok. |
| Unknown | `1` | Bilinmeyen bir görüntü türü veya Microsoft Word belgesinde doğrudan depolanamayan görüntü türü. |
| Emf | `2` | Windows Geliştirilmiş Meta Dosyası. |
| Wmf | `3` | Windows Meta Dosyası. |
| Pict | `4` | Macintosh PICT. Mevcut bir görüntü bir belgede korunacaktır ancak yeni PICT görüntülerinin bir belgeye eklenmesi desteklenmez. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Taşınabilir Ağ Grafikleri. |
| Bmp | `7` | Windows Bitmap. |
| Eps | `8` | Encapsulated PostScript. |

## Örnekler

Bir şekle nasıl resim ekleneceğini ve tipinin nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // URL'deki resim bir .gif'tir. Bunu bir belgeye eklemek, onu bir .png dosyasına dönüştürür.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Ayrıca bakınız

* property [ImageType](../imagedata/imagetype/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
