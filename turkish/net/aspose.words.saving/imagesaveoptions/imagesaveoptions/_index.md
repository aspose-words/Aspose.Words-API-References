---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: .NET için Aspose.Words
description: Görüntüleri TIFF, PNG, BMP, JPEG, EMF, EPS, WebP ve SVG gibi çok yönlü formatlarda kaydetmek için ImageSaveOptions oluşturucusunu keşfedin. Görüntü işlemeyi optimize edin!
type: docs
weight: 10
url: /tr/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Bu sınıfın, işlenmiş görüntüleri içinde kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP veyaSvg biçim.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | Olabilir Tiff ,Png ,Bmp , Jpeg ,Emf ,EpsWebP veyaSvg biçim. |

## Örnekler

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Belgeyi işlerken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu küçültecektir, ancak görüntü daha belirgin sıkıştırma eserleri gösterecektir.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, dosya boyutunun artması pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
