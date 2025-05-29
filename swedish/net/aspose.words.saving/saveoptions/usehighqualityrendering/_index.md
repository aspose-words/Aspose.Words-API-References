---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words för .NET
description: Optimera dina SaveOptions med egenskapen UseHighQualityRendering för överlägsen resultat. Kontrollera renderingshastighet och kvalitet för perfekta resultat.
type: docs
weight: 210
url: /sv/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte.

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

Den här egenskapen används när dokumentet exporteras till bildformaten: Tiff ,Png ,Bmp , Jpeg ,Emf.

## Exempel

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
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
