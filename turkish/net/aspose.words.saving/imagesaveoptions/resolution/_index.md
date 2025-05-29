---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: .NET için Aspose.Words
description: Görüntülerinizi ImageSaveOptions ile optimize edin! Çarpıcı kalite ve netlik için yatay ve dikey çözünürlüğü DPI olarak kontrol edin. Görsellerinizi bugün geliştirin!
type: docs
weight: 130
url: /tr/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

Oluşturulan görüntüler için hem yatay hem de dikey çözünürlüğü inç başına nokta cinsinden ayarlar.

```csharp
public float Resolution { set; }
```

## Notlar

Bu özellik yalnızca raster görüntü formatlarına kaydedilirken etkilidir.

## Örnekler

Bir belgeyi PNG'ye dönüştürürken çözünürlüğün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "ImageSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi görüntüye dönüştürme şeklini değiştirmek için.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Belgeyi 72 dpi olarak görüntülemek için "Çözünürlük" özelliğini "72" olarak ayarlayın.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Belgeyi 300 dpi olarak işlemek için "Çözünürlük" özelliğini "300" olarak ayarlayın.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### Ayrıca bakınız

* class [ImageSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
