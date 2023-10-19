---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words for .NET
description: ImageSaveOptions PixelFormat mülk. Oluşturulan görüntülerin piksel biçimini alır veya ayarlar C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

Oluşturulan görüntülerin piksel biçimini alır veya ayarlar.

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## Notlar

Bu özellik yalnızca taramalı görüntü formatlarına kaydederken etkilidir.

Varsayılan değer:Format32BppArgb.

Çıkış görüntüsünün piksel biçimi, GDI+ çalışması nedeniyle ayarlanan değerden farklı olabilir.

## Örnekler

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

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
