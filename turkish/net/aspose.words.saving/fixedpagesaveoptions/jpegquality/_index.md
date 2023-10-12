---
title: FixedPageSaveOptions.JpegQuality
second_title: Aspose.Words for .NET API Referansı
description: FixedPageSaveOptions mülk. Html belgesindeki JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

Html belgesindeki JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar.

```csharp
public int JpegQuality { get; set; }
```

### Notlar

Yalnızca bir belge JPEG görüntüleri içerdiğinde etkili olur.

Sabit sayfa formatında kaydederken bir belge içindeki görüntülerin kalitesini elde etmek veya ayarlamak için bu özelliği kullanın. Değer 0 ila 100 arasında değişebilir; burada 0, en kötü kalite ancak maksimum sıkıştırma anlamına gelir ve 100 , en iyi kalite ancak minimum sıkıştırma anlamına gelir.

Varsayılan değer 95'tir.

### Örnekler

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

* class [FixedPageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* toplantı [Aspose.Words](../../../)


