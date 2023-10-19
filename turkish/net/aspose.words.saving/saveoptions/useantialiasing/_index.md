---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words for .NET
description: SaveOptions UseAntiAliasing mülk. Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Oluşturma için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` . Bu değer şu şekilde ayarlandığında`doğru` kenar yumuşatma is oluşturma için kullanılır.

Bu özellik, belge şu formatlara aktarıldığında kullanılır: Tiff ,Png ,Bmp , Jpeg ,Emf . Belge the 'ye aktarıldığındaHtml ,Mhtml , Epub ,Azw3 veyaMobi formatlarında bu seçenek raster görüntüler için kullanılır.

## Örnekler

İşlenen bir belgenin kalitesinin SaveOptions ile nasıl iyileştirileceğini gösterir.

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
