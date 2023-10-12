---
title: ImageSaveOptions.ImageBrightness
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Oluşturulan görüntülerin parlaklığını alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/imagesaveoptions/imagebrightness/
---
## ImageSaveOptions.ImageBrightness property

Oluşturulan görüntülerin parlaklığını alır veya ayarlar.

```csharp
public float ImageBrightness { get; set; }
```

### Notlar

Bu özellik yalnızca taramalı görüntü formatlarına kaydederken etkilidir.

Varsayılan değer 0,5'tir. Değer 0 ile 1 arasında olmalıdır.

### Örnekler

Aspose.Words bir belgeyi belgeye dönüştürürken görüntünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi resim olarak kaydettiğimizde, bir SaveOptions nesnesini iletebiliriz
// kaydetme işlemi onu oluştururken görüntüyü düzenleyin.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Görüntünün parlaklığını ve kontrastını değiştirmek için bu özellikleri ayarlayabiliriz.
    // Her ikisi de 0-1 ölçeğindedir ve varsayılan olarak 0,5'tir.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Bu özelliklerle yatay ve dikey çözünürlüğü ayarlayabiliriz.
    // Bu görüntünün boyutlarını etkileyecektir.
    // Bu özelliklerin varsayılan değeri 96 dpi çözünürlük için 96,0'dır.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Bu özelliği kullanarak görüntüyü ölçeklendirebiliriz. %100 ölçeklendirme için varsayılan değer 1,0'dır.
    // Bu özelliği, çözünürlük değişikliğinin görüntü boyutlarında neden olacağı değişiklikleri engellemek için kullanabiliriz.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


