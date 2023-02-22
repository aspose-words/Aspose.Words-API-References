---
title: SaveOptions.UseAntiAliasing
second_title: Aspose.Words för .NET API Referens
description: SaveOptions fast egendom. Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering.
type: docs
weight: 210
url: /sv/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering.

```csharp
public bool UseAntiAliasing { get; set; }
```

### Anmärkningar

Standardvärdet är`falsk` . När detta värde är satt till`Sann` kantutjämning används för rendering.

Den här egenskapen används när dokumentet exporteras till följande format: Tiff ,Png ,Bmp , Jpeg ,Emf . När dokumentet exporteras till Html ,Mhtml ochEpub formats detta alternativ används för rasterbilder.

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


