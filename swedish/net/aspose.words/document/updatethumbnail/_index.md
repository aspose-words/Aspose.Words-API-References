---
title: Document.UpdateThumbnail
linktitle: UpdateThumbnail
articleTitle: UpdateThumbnail
second_title: Aspose.Words för .NET
description: Uppdatera enkelt miniatyrbilden av ditt dokument med våra anpassningsbara alternativ. Förbättra dina bilder och dokumentpresentationen idag!
type: docs
weight: 840
url: /sv/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(*[ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)*) {#updatethumbnail_1}

Uppdateringar[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) av dokumentet enligt de angivna alternativen.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Genereringsalternativen att använda. |

## Anmärkningar

Den[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) låter dig ange källan för miniatyrbilden, storlek och andra alternativ. Om försöket att generera miniatyrbilden misslyckas ändras ingen.

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Uppdateringar[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) av dokumentet med standardalternativen.

```csharp
public void UpdateThumbnail()
```

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

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
