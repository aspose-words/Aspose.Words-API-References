---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words för .NET
description: ThumbnailGeneratingOptions GenerateFromFirstPage fast egendom. Anger om miniatyrbilden ska genereras från första sidan i dokumentet eller första bilden i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

Anger om miniatyrbilden ska genereras från första sidan i dokumentet eller första bilden.

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## Anmärkningar

Standard är`Sann` , vilket innebär att miniatyrbilden kommer att genereras från första sidan i dokumentet. Om värdet är`falsk` och det finns ingen bild i dokumentet kommer miniatyrbilden att genereras från första sidan i dokumentet.

## Exempel

Visar hur man uppdaterar ett dokuments miniatyrbild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Det finns två sätt att ställa in en miniatyrbild när du sparar ett dokument i .epub.
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
