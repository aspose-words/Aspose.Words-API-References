---
title: ImageSaveOptions.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: .NET için Aspose.Words
description: Çarpıcı görseller için DPI'da görüntü kalitesini kolayca ayarlamak ve optimize etmek üzere ImageSaveOptions VerticalResolution özelliğini keşfedin. Projelerinizi bugün geliştirin!
type: docs
weight: 200
url: /tr/net/aspose.words.saving/imagesaveoptions/verticalresolution/
---
## ImageSaveOptions.VerticalResolution property

Oluşturulan görüntülerin dikey çözünürlüğünü inç başına nokta cinsinden alır veya ayarlar.

```csharp
public float VerticalResolution { get; set; }
```

## Notlar

Bu özellik yalnızca raster görüntü biçimlerine kaydederken etkilidir ve çıktı boyutunu piksel cinsinden etkiler.

Varsayılan değer 96'dır.

## Örnekler

Aspose.Words'ün bir belgeyi bir belgeye dönüştürmesini sağlarken görüntünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Belgeyi bir resim olarak kaydettiğimizde, SaveOptions nesnesini görüntüye geçirebiliriz.
// Kaydetme işlemi sırasında görüntüyü düzenle.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Görüntünün parlaklığını ve kontrastını değiştirmek için bu özellikleri ayarlayabiliriz.
    // Her ikisi de 0-1 ölçeğindedir ve varsayılan olarak 0,5'tir.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Bu özellikler ile yatay ve dikey çözünürlüğü ayarlayabiliriz.
    // Bu, görüntünün boyutlarını etkileyecektir.
    // Bu özelliklerin varsayılan değeri 96 dpi çözünürlük için 96.0'dır.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Bu özelliği kullanarak görüntüyü ölçekleyebiliriz. Varsayılan değer %100 ölçekleme için 1.0'dır.
    // Bu özelliği, çözünürlüğü değiştirmenin görüntü boyutlarında neden olacağı değişiklikleri ortadan kaldırmak için kullanabiliriz.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
