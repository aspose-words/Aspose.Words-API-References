---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: .NET için Aspose.Words
description: Üstün çıktı için UseHighQualityRendering özelliğiyle SaveOptions'ınızı optimize edin. Mükemmel sonuçlar için işleme hızını ve kalitesini kontrol edin.
type: docs
weight: 210
url: /tr/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Yüksek kaliteli (yani yavaş) işleme algoritmalarının kullanılıp kullanılmayacağını belirleyen bir değeri alır veya ayarlar.

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

Bu özellik, belge görüntü biçimlerine aktarıldığında kullanılır: Tiff ,Png ,Bmp , Jpeg ,Emf.

## Örnekler

SaveOptions ile işlenmiş bir belgenin kalitesinin nasıl iyileştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
