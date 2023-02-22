---
title: Class ImageSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.ImageSaveOptions klass. Gör det möjligt att ange ytterligare alternativ när du renderar dokumentsidor eller former till bilder.
type: docs
weight: 4970
url: /sv/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Gör det möjligt att ange ytterligare alternativ när du renderar dokumentsidor eller former till bilder.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | Initierar en ny instans av denna klass som kan användas för att spara renderade bilder i Tiff ,Png ,Bmp , Emf ,Jpeg ellerSvg format. Png ,Bmp ,Jpeg ellerSvg format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur färger återges. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Endast som standardFlatOpc dokumentformat får mappas. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Tillåter att ange renderingsläge och kvalitet förGraphics objekt. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Hämtar eller ställer in den horisontella upplösningen för de genererade bilderna, i punkter per tum. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Hämtar eller ställer in ljusstyrkan för de genererade bilderna. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Hämtar eller ställer in färgläget för de genererade bilderna. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Hämtar eller ställer in kontrasten för de genererade bilderna. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer kvaliteten på de genererade JPEG-bilderna. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Tillåter att ange hur metafiler behandlas i den renderade utdata. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat/) används för återgivning av siffror. Europeiska siffror används som standard. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flagga indikerar om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort, sammanlänkas även grannglyfer med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är inställd på true. Standard är false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Hämtar eller ställer in sidorna att rendera. Standard är alla sidor i dokumentet. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Hämtar eller ställer in bakgrundsfärgen (papper) för de genererade bilderna. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Hämtar eller ställer in pixelformatet för de genererade bilderna. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Ställer in både horisontell och vertikal upplösning för de genererade bilderna, i punkter per tum. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Anger formatet som de renderade dokumentsidorna eller formerna kommer att sparas i om detta sparaalternativ-objekt används. Kan vara ett raster Tiff ,Png ,Bmp , Jpeg eller vektorEmf ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Hämtar eller ställer in zoomfaktorn för de genererade bilderna. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Hämtar eller ställer in tröskeln som bestämmer värdet för binariseringsfelet i Floyd-Steinberg-metoden. när[`ImageBinarizationMethod`](../imagebinarizationmethod/) är ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Hämtar eller ställer in metod som används vid konvertering av bilder till 1 bpp format när[`SaveFormat`](./saveformat/) är SaveFormat.Tiff and [`TiffCompression`](./tiffcompression/) är lika med TiffCompression.Ccitt3 eller TiffCompression.Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Hämtar eller ställer in vilken typ av komprimering som ska tillämpas när genererade bilder sparas i TIFF-formatet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | Hämtar eller ställer in ett värde som avgör om GDI+ eller Aspose.Words-metafilrenderare ska användas när du sparar till EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Hämtar eller ställer in den vertikala upplösningen för de genererade bilderna, i punkter per tum. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Skapar en djup klon av detta objekt. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Bestämmer om det angivna objektet har samma värde som det aktuella objektet. |

### Exempel

Återger en sida i ett Word-dokument till en bild med transparent eller färgad bakgrund.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Ställ in egenskapen "PaperColor" till en transparent färg för att tillämpa en transparent
// bakgrund till dokumentet medan du renderar det till en bild.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Ställ in egenskapen "PaperColor" till en ogenomskinlig färg för att tillämpa den färgen
// som bakgrund för dokumentet när vi renderar det till en bild.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Visar hur du konfigurerar komprimering medan du sparar ett dokument som en JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Ställ in egenskapen "JpegQuality" till "10" för att använda starkare komprimering när du renderar dokumentet.
// Detta kommer att minska filstorleken på dokumentet, men bilden kommer att visa mer framträdande komprimeringsartefakter.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Ställ in egenskapen "JpegQuality" till "100" för att använda svagare komprimering när du renderar dokumentet.
// Detta kommer att förbättra kvaliteten på bilden till priset av en ökad filstorlek.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Visar hur man anger en upplösning när ett dokument renderas till PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
            // för att ändra sättet på vilket den metoden renderar dokumentet till en bild.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Ställ in egenskapen "Resolution" till "72" för att återge dokumentet i 72dpi.
            options.Resolution = 72;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

            Assert.That(120000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png").Length));

#if NET48 || JAVA
            Image image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png");

            Assert.AreEqual(612, image.Width);
            Assert.AreEqual(792, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png")) 
            {
                Assert.AreEqual(612, image.Width);
                Assert.AreEqual(792, image.Height);
            }
#endif
            // Ställ in egenskapen "Resolution" till "300" för att återge dokumentet i 300 dpi.
            options.Resolution = 300;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);

            Assert.That(700000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png").Length));

#if NET48 || JAVA
            image = Image.FromFile(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png");

            Assert.AreEqual(2550, image.Width);
            Assert.AreEqual(3300, image.Height);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png")) 
            {
                Assert.AreEqual(2550, image.Width);
                Assert.AreEqual(3300, image.Height);
            }
#endif
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


