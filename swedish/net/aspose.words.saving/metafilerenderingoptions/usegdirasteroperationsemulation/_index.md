---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words för .NET
description: Upptäck egenskapen UseGdiRasterOperationsEmulation i MetafileRenderingOptions för att optimera rasteroperationer med GDI. Förbättra prestanda och flexibilitet idag!
type: docs
weight: 80
url: /sv/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

Hämtar eller ställer in ett värde som avgör om GDI+ ska användas för rasteroperationsemulering.

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## Anmärkningar

Windows GDI+-biblioteket kan användas för att emulera rasteroperationer. Det ger stöd för alla rasteroperationer jämfört med Aspose.Words egen emulering, men prestandan kan vara långsammare i vissa fall.

När detta värde är inställt på`sann`Aspose.Words använder GDI+ för emulering av rasteroperationer.

När detta värde är inställt på`falsk`Aspose.Words använder sin egen implementering av rasteroperationsemulering.

Det här alternativet används endast när metafilen återges som vektorgrafik.

Standardvärdet är`falsk`.

## Exempel

Visar hur man ställer in renderingsläget när man sparar dokument med Windows Metafile-bilder till andra bildformat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
// bestäm hur sparoperationen ska bearbeta Windows-metafiler i dokumentet.
// Om vi ställer in egenskapen "RenderingMode" till "MetafileRenderingMode.Vector",
// eller "MetafileRenderingMode.VectorWithFallback", kommer vi att rendera alla metafiler som vektorgrafik.
// Om vi ställer in egenskapen "RenderingMode" till "MetafileRenderingMode.Bitmap" kommer vi att rendera alla metafiler som bitmappar.
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
