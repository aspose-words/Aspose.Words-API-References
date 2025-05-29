---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words för .NET
description: Upptäck hur alternativet GenerateFromFirstPage skapar miniatyrbilder från dokumentets första sida eller bild, vilket enkelt förbättrar ditt visuella innehåll.
type: docs
weight: 20
url: /sv/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Anger om miniatyrbilden ska genereras från dokumentets första sida eller den första bilden.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Anmärkningar

Standard är`sann` , vilket innebär att miniatyrbilden genereras från dokumentets första sida. Om värdet är`falsk` och det inte finns någon bild i dokumentet genereras en miniatyrbild från dokumentets första sida.

## Exempel

Visar hur man uppdaterar en dokumentminiatyr.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Det finns två sätt att ange en miniatyrbild när man sparar ett dokument till .epub.
// 1 - Använd dokumentets första sida:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Använd den första bilden som finns i dokumentet:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Se även

* class [ThumbnailGeneratingOptions](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
