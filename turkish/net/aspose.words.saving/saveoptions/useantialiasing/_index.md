---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: .NET için Aspose.Words
description: İşleme kalitenizi artırmak için SaveOptions UseAntiAliasing özelliğini keşfedin. Daha akıcı görseller ve gelişmiş performans için kenar yumuşatmayı kontrol edin.
type: docs
weight: 200
url: /tr/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

İşleme için kenar yumuşatma kullanılıp kullanılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` Bu değer olarak ayarlandığında`doğru` anti-aliasing is işleme için kullanılır.

Bu özellik, belge aşağıdaki biçimlerde dışa aktarıldığında kullanılır: Tiff ,Png ,Bmp , Jpeg ,Emf Belge the 'ye aktarıldığındaHtml ,Mhtml , Epub ,Azw3 veyaMobiBiçimler Bu seçenek raster görüntüler için kullanılır.

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
