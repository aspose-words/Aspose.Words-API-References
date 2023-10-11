---
title: Enum ImageColorMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.ImageColorMode Sıralama. Belge sayfalarının oluşturulan görüntüleri için renk modunu belirtir.
type: docs
weight: 5210
url: /tr/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

Belge sayfalarının oluşturulan görüntüleri için renk modunu belirtir.

```csharp
public enum ImageColorMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belgenin sayfaları renkli resimler olarak gösterilecektir. |
| Grayscale | `1` | Belgenin sayfaları gri tonlamalı resimler olarak oluşturulacaktır. |
| BlackAndWhite | `2` | Belgenin sayfaları siyah beyaz resimler olarak gösterilecektir. |

### Örnekler

Belgeleri işlerken renk modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Belgeyi resim olarak kaydettiğimizde, bir SaveOptions nesnesini iletebiliriz
            // kaydetme işleminin oluşturacağı görüntü için bir renk modu seçin.
            // "ImageColorMode" özelliğini "ImageColorMode.BlackAndWhite" olarak ayarlarsak,
            // kaydetme işlemi, belge oluşturulurken gri tonlamalı renk azaltma uygulayacaktır.
            // "ImageColorMode" özelliğini "ImageColorMode.Grayscale" olarak ayarlarsak,
            // kaydetme işlemi belgeyi tek renkli bir görüntüye dönüştürecektir.
            // "ImageColorMode" özelliğini "None" olarak ayarlarsak kaydetme işlemi varsayılan yöntemi uygulayacaktır
            // ve çıktı görüntüsündeki tüm belgenin renklerini koruyun.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


