---
title: ImageSaveOptions.ImageSize
second_title: Aspose.Words for .NET API Referansı
description: ImageSaveOptions mülk. Oluşturulan görüntünün boyutunu piksel cinsinden alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

Oluşturulan görüntünün boyutunu piksel cinsinden alır veya ayarlar.

```csharp
public Size ImageSize { get; set; }
```

### Notlar

Bu özellik yalnızca taramalı görüntü formatlarına kaydederken etkilidir.

Varsayılan değer (0 x 0)'dır; bu, oluşturulan görüntünün boyutunun, görüntünün nokta cinsinden boyutuna, belirtilen çözünürlüğe ve ölçeğe göre hesaplanacağı anlamına gelir.

### Örnekler

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

// Belgenin "Save" yöntemine aktarabileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi bir görüntüye dönüştürme biçimini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // "PageSet" özelliğini ilk sayfanın numarasına ayarlayın
    // belgenin görüntülenmeye nereden başlayacağı.
    options.PageSet = new PageSet(i);
    // Sayfayı 2325x5325 piksel ve 600 dpi çözünürlükte dışa aktarın.
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../imagesaveoptions/)
* toplantı [Aspose.Words](../../../)


