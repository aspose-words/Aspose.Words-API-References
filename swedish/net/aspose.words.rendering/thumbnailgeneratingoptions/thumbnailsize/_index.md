---
title: ThumbnailGeneratingOptions.ThumbnailSize
second_title: Aspose.Words för .NET API Referens
description: ThumbnailGeneratingOptions fast egendom. Storlek på genererad miniatyrbild i pixlar. Standard är 600x900.
type: docs
weight: 30
url: /sv/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

Storlek på genererad miniatyrbild i pixlar. Standard är 600x900.

```csharp
public Size ThumbnailSize { get; set; }
```

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

* class [ThumbnailGeneratingOptions](../)
* namnutrymme [Aspose.Words.Rendering](../../thumbnailgeneratingoptions/)
* hopsättning [Aspose.Words](../../../)


