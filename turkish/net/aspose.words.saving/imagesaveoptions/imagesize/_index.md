---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: .NET için Aspose.Words
description: En iyi sonuçları elde etmek için görüntü boyutlarını piksel cinsinden kolayca yönetmek ve özelleştirmek üzere ImageSaveOptions'ın ImageSize özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Oluşturulan bir görüntünün boyutunu piksel cinsinden alır veya ayarlar.

```csharp
public Size ImageSize { get; set; }
```

## Notlar

Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkilidir.

Varsayılan değer (0 x 0)'dır, yani oluşturulan görüntünün boyutu, görüntünün nokta cinsinden boyutuna, belirtilen çözünürlüğe ve ölçeğe göre x000d olarak hesaplanacaktır.

## Örnekler

Bir belgenin her sayfasının ayrı bir TIFF görüntüsüne nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // "PageSet" özelliğini ilk sayfanın numarasına ayarlayın
    // belgenin hangisinden oluşturulmaya başlanacağı.
    options.PageSet = new PageSet(i);
    // Sayfayı 2325x5325 piksel ve 600 dpi olarak dışa aktar.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
