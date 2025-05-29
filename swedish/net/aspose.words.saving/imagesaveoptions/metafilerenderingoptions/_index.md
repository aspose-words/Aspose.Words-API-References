---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageSaveOptions MetafileRenderingOptions för att styra metafilhanteringen i din renderade utdata för förbättrad bildkvalitet.
type: docs
weight: 90
url: /sv/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

Gör det möjligt att ange hur metafiler behandlas i den renderade utdatan.

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## Anmärkningar

NärVector är specificerat, renderar Aspose.Words först metafil till vektorgrafik med hjälp av sin egen renderingsmotor för metafiler och render sedan vector -grafik till bilden.

NärBitmap är specificerat, renderar Aspose.Words metafilen direkt till bilden med hjälp av GDI+-renderingsmotorn för metafil.

GDI+ metafilrenderingsmotorn fungerar snabbare, stöder nästan alla metafilfunktioner, men vid låga upplösningar kan den ge inkonsekventa resultat jämfört med resten av vektorgrafiken (särskilt för text) på sidan. Aspose.Words metafilrenderingsmotor ger ett mer konsekvent resultat även vid låga upplösningar, men den fungerar långsammare och kan rendera komplexa metafiler felaktigt.

Standardvärdet för[`MetafileRenderingMode`](../../metafilerenderingmode/) ärBitmap.

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

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
