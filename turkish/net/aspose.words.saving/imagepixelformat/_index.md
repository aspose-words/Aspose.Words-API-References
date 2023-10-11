---
title: Enum ImagePixelFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.ImagePixelFormat Sıralama. Belge sayfalarının oluşturulan görüntüleri için piksel biçimini belirtir.
type: docs
weight: 5220
url: /tr/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

Belge sayfalarının oluşturulan görüntüleri için piksel biçimini belirtir.

```csharp
public enum ImagePixelFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Format16BppRgb555 | `0` | Piksel başına 16 bit, RGB. |
| Format16BppRgb565 | `1` | Piksel başına 16 bit, RGB. |
| Format16BppArgb1555 | `2` | Piksel başına 16 bit, ARGB. |
| Format24BppRgb | `3` | Piksel başına 24 bit, RGB. |
| Format32BppRgb | `4` | Piksel başına 32 bit, RGB. |
| Format32BppArgb | `5` | Piksel başına 32 bit, ARGB. |
| Format32BppPArgb | `6` | Piksel başına 32 bit, ARGB, önceden çarpılmış alfa. |
| Format48BppRgb | `7` | Piksel başına 48 bit, RGB. |
| Format64BppArgb | `8` | Piksel başına 64 bit, ARGB. |
| Format64BppPArgb | `9` | Piksel başına 64 bit, ARGB, önceden çarpılmış alfa. |
| Format1bppIndexed | `10` | Piksel başına 1 bit, Dizine Alınmış. |

### Örnekler

Bir belgenin görüntüye dönüştürüleceği piksel başına bit oranının nasıl seçileceğini gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Belgeyi resim olarak kaydettiğimizde, bir SaveOptions nesnesini iletebiliriz
            // kaydetme işleminin oluşturacağı görüntü için bir piksel formatı seçin.
            // Piksel başına çeşitli bit oranları, oluşturulan görüntünün kalitesini ve dosya boyutunu etkileyecektir.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // ImageSaveOptions örneklerini klonlayabiliriz.
            Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

            doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format32BppRgb:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(70000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                case ImagePixelFormat.Format32BppRgb:
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#endif
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


