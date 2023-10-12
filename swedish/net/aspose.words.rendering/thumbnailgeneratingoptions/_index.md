---
title: Class ThumbnailGeneratingOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions klass. Kan användas för att ange ytterligare alternativ vid generering av miniatyrbilder för ett dokument.
type: docs
weight: 4600
url: /sv/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

Kan användas för att ange ytterligare alternativ vid generering av miniatyrbilder för ett dokument.

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
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | Anger om miniatyrbilden ska genereras från första sidan i dokumentet eller första bilden. |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | Storlek på genererad miniatyrbild i pixlar. Standard är 600x900. |

### Anmärkningar

Användaren kan anropa metod[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/) att generera [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) för ett dokument.

### Exempel

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

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)


