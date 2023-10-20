---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words for .NET
description: ImageSaveOptions JpegQuality mülk. Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar.

```csharp
public int JpegQuality { get; set; }
```

## Notlar

Yalnızca JPEG'e kaydederken etkilidir.

JPEG biçiminde kaydederken oluşturulan görüntülerin kalitesini almak veya ayarlamak için bu özelliği kullanın. Değer 0 ila 100 arasında değişebilir; burada 0, en kötü kalite ancak maksimum sıkıştırma anlamına gelir ve 100 , en iyi kalite ancak minimum sıkıştırma anlamına gelir.

Varsayılan değer 95'tir.

## Örnekler

Bir belgeyi JPEG olarak kaydederken sıkıştırmanın nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Belgeyi oluştururken daha güçlü sıkıştırma kullanmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
// Bu, belgenin dosya boyutunu azaltacaktır ancak görüntü, sıkıştırma kusurlarını daha belirgin bir şekilde görüntüleyecektir.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Belgeyi işlerken daha zayıf sıkıştırma kullanmak için "JpegQuality" özelliğini "100" olarak ayarlayın.
// Bu, dosya boyutunun artması pahasına görüntünün kalitesini artıracaktır.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
