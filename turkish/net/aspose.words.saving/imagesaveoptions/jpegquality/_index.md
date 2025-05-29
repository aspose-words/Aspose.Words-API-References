---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: .NET için Aspose.Words
description: Çarpıcı görseller ve gelişmiş performans için JPEG görüntü kalitesini optimize etmek üzere ImageSaveOptions'daki JpegQuality özelliğini ayarlayın. Geliştiriciler için mükemmel!
type: docs
weight: 80
url: /tr/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

Oluşturulan JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar.

```csharp
public int JpegQuality { get; set; }
```

## Notlar

Sadece JPEG olarak kaydedildiğinde etkilidir.

JPEG formatında kaydederken oluşturulan görüntülerin kalitesini almak veya ayarlamak için bu özelliği kullanın. Değer 0 ile 100 arasında değişebilir; burada 0 en kötü kalite ancak maksimum sıkıştırma anlamına gelirken, 100 en iyi kalite ancak minimum sıkıştırma anlamına gelir.

Varsayılan değer 95'tir.

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

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
