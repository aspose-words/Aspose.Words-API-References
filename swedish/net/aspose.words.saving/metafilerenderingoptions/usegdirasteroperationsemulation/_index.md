---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words för .NET
description: MetafileRenderingOptions UseGdiRasterOperationsEmulation fast egendom. Hämtar eller ställer in ett värde som avgör om GDI ska användas eller inte för emulering av rasteroperationer i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Hämtar eller ställer in ett värde som avgör om GDI+ ska användas eller inte för emulering av rasteroperationer.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Anmärkningar

Windows GDI+-bibliotek kan användas för att emulera rasteroperationer. Det ger stöd för all raster operation jämfört med Aspose.Words egen emulering men prestandan kan vara långsammare i vissa fall.

När detta värde är satt till`Sann`, Aspose.Words använder GDI+ för emulering av rasteroperationer.

När detta värde är satt till`falsk`, Aspose.Words använder sin egen implementering av emulering av rasteroperationer.

Det här alternativet används endast när metafilen renderas som vektorgrafik.

Standardvärdet är`falsk`.

## Exempel

Visar hur du ställer in renderingsläget när du sparar dokument med Windows Metafile-bilder till andra bildformat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(Image.FromFile(ImageDir + "Windows MetaFile.wmf"));

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
// bestäm hur sparoperationen kommer att bearbeta Windows-metafiler i dokumentet.
// Om vi ställer in egenskapen "RenderingMode" till "MetafileRenderingMode.Vector",
// eller "MetafileRenderingMode.VectorWithFallback", vi kommer att rendera alla metafiler som vektorgrafik.
// Om vi ställer in egenskapen "RenderingMode" till "MetafileRenderingMode.Bitmap", renderar vi alla metafiler som bitmappar.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// Aspose.Words använder GDI+ för emulering av rasteroperationer, när värdet är satt till sant.
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### Se även

* class [MetafileRenderingOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
