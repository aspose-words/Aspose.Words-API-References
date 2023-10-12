---
title: SaveOptions.UseHighQualityRendering
second_title: Aspose.Words för .NET API Referens
description: SaveOptions fast egendom. Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa dvs långsamma renderingsalgoritmer ska användas eller inte.
type: docs
weight: 200
url: /sv/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte.

```csharp
public bool UseHighQualityRendering { get; set; }
```

### Anmärkningar

Standardvärdet är`falsk` .

Den här egenskapen används när dokumentet exporteras till bildformat: Tiff ,Png ,Bmp , Jpeg ,Emf.

### Exempel

Visar hur man förbättrar kvaliteten på ett renderat dokument med SaveOptions.

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

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../saveoptions/)
* hopsättning [Aspose.Words](../../../)


