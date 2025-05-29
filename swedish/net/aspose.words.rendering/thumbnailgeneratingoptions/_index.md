---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Rendering.ThumbnailGeneratingOptions för att förbättra genereringen av dokumentminiatyrer med anpassningsbara funktioner och förbättrad kvalitet.
type: docs
weight: 5330
url: /sv/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Kan användas för att ange ytterligare alternativ när miniatyrbilder genereras för ett dokument.

```csharp
public class ThumbnailGeneratingOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Anger om miniatyrbilden ska genereras från dokumentets första sida eller den första bilden. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Storlek på genererad miniatyrbild i pixlar. Standard är 600x900. |

## Anmärkningar

Användaren kan anropa metoden[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) att generera [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) för ett dokument.

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

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
