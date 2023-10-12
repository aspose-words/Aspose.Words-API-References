---
title: ImageSaveOptions.MetafileRenderingOptions
second_title: Aspose.Words för .NET API Referens
description: ImageSaveOptions fast egendom. Tillåter att ange hur metafiler behandlas i den renderade utdata.
type: docs
weight: 90
url: /sv/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Tillåter att ange hur metafiler behandlas i den renderade utdata.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

### Anmärkningar

NärVector anges, renderar Aspose.Words metafil till vektorgrafik med sin egen metafil-renderingsmotor först och renderar sedan vektor -grafik till bilden.

NärBitmap anges, renderar Aspose.Words metafil direkt till bilden med hjälp av GDI+ metafil renderingsmotor.

GDI+-metafilrenderingsmotorn fungerar snabbare, stöder nästan alla metafilfunktioner men på low upplösningar kan det ge inkonsekventa resultat jämfört med resten av vektorgrafik (särskilt för text) på sidan. Aspose.Words-metafilrenderingsmotorn kommer att ge mer konsekventa resultat even på låga upplösningar men fungerar långsammare och kan rendera komplexa metafiler felaktigt.

Standardvärdet för[`MetafileRenderingMode`](../../metafilerenderingmode/) ärBitmap.

### Exempel

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../imagesaveoptions/)
* hopsättning [Aspose.Words](../../../)


