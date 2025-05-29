---
title: ImageSaveOptions Class
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.ImageSaveOptions. Rendera enkelt dina dokument med anpassningsbara alternativ för högkvalitativ bildutskrift.
type: docs
weight: 5980
url: /sv/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Gör det möjligt att ange ytterligare alternativ vid rendering av dokumentsidor eller former till bilder.

För att lära dig mer, besök[Ange alternativ för sparning](https://docs.aspose.com/words/net/specify-save-options/) dokumentationsartikel.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initierar en ny instans av den här klassen som kan användas för att spara renderade bilder i Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps , WebP ellerSvg format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om inbäddning av teckensnitt med PostScript-konturer ska tillåtas när TrueType-teckensnitt bäddas in i ett dokument när det sparas. Standardvärdet är`falsk` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur färger återges. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in en anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller anger sökvägen till standardmallen (inklusive filnamn). Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-former renderas. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När`sann` , gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är`sann` . |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Gör det möjligt att ange renderingsläge och kvalitet förGraphics objekt. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Hämtar eller ställer in den horisontella upplösningen för de genererade bilderna, i punkter per tum. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Hämtar eller ställer in ljusstyrkan för de genererade bilderna. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Hämtar eller ställer in färgläget för de genererade bilderna. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Hämtar eller ställer in kontrasten för de genererade bilderna. |
| [ImageSize](../../aspose.words.saving/imagesaveoptions/imagesize/) { get; set; } | Hämtar eller ställer in storleken på en genererad bild i pixlar. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer kvaliteten på de genererade JPEG-bilderna. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Gör det möjligt att ange hur metafiler behandlas i den renderade utdatan. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat/) används för rendering av siffror. Europeiska siffror används som standard. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flaggan anger om det är nödvändigt att optimera utdata. Om denna flagga är inställd tas redundanta kapslade arbetsytor och tomma arbetsytor bort, sammanfogas även angränsande tecken med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas om den här egenskapen är inställd på`sann` . Standard är`falsk` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till ett fast sidformat. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Hämtar eller ställer in sidorna som ska renderas. Standard är alla sidor i dokumentet. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Hämtar eller ställer in bakgrundsfärgen (pappersfärgen) för de genererade bilderna. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Hämtar eller ställer in pixelformatet för de genererade bilderna. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om sparningsförloppet. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Ställer in både horisontell och vertikal upplösning för de genererade bilderna, i punkter per tum. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Anger formatet i vilket de renderade dokumentsidorna eller formerna sparas om det här objektet för sparade alternativ används. Kan vara ett raster Tiff ,Png ,Bmp , Jpeg eller vektorEmf ,Eps , WebP ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Hämtar eller ställer in zoomfaktorn för de genererade bilderna. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Hämtar eller ställer in tröskelvärdet som bestämmer värdet för binariseringsfelet i Floyd-Steinberg-metoden. när[`ImageBinarizationMethod`](../imagebinarizationmethod/) ärFloydSteinbergDithering . |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Hämtar eller ställer in metoden som används vid konvertering av bilder till 1 bpp-format när[`SaveFormat`](./saveformat/) ärTiff och [`TiffCompression`](./tiffcompression/) är lika medCcitt3 ellerCcitt4 . |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Hämtar eller ställer in vilken typ av komprimering som ska tillämpas när genererade bilder sparas i TIFF-format. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om antialiasing ska användas för rendering. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | Hämtar eller anger ett värde som avgör om GDI+ eller Aspose.Words metafilrenderare ska användas vid sparning till EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Hämtar eller ställer in den vertikala upplösningen för de genererade bilderna, i punkter per tum. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Skapar en djup klon av detta objekt. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man anger en upplösning när man renderar ett dokument till PNG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// Ställ in egenskapen "Upplösning" till "72" för att rendera dokumentet i 72 dpi.
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// Ställ in egenskapen "Upplösning" till "300" för att rendera dokumentet i 300 dpi.
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

Visar hur man konfigurerar komprimering när man sparar ett dokument som JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// Sätt egenskapen "JpegQuality" till "10" för att använda starkare komprimering vid rendering av dokumentet.
// Detta minskar dokumentets filstorlek, men bilden kommer att visa mer framträdande komprimeringsartefakter.
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Sätt egenskapen "JpegQuality" till "100" för att använda svagare komprimering vid rendering av dokumentet.
// Detta kommer att förbättra bildens kvalitet till bekostnad av en ökad filstorlek.
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

Återger en sida från ett Word-dokument till en bild med transparent eller färgad bakgrund.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Skapa ett "ImageSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att modifiera hur metoden renderar dokumentet till en bild.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// Ställ in egenskapen "PaperColor" till en transparent färg för att tillämpa en transparent färg
// bakgrund till dokumentet när det renderas till en bild.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Ställ in egenskapen "PaperColor" till en ogenomskinlig färg för att tillämpa den färgen
// som bakgrund för dokumentet när vi renderar det till en bild.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
