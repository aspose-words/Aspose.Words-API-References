---
title: Class ImageSaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.ImageSaveOptions klas. Ermöglicht die Angabe zusätzlicher Optionen beim Rendern von Dokumentseiten oder Formen in Bilder.
type: docs
weight: 5230
url: /de/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim Rendern von Dokumentseiten oder Formen in Bilder.

Um mehr zu erfahren, besuchen Sie die[Geben Sie Speicheroptionen an](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern gerenderter Bilder im verwendet werden kann.Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps oderSvg format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Umrissen zulässig ist , wenn TrueType-Schriftarten in ein Dokument eingebettet werden, sobald es gespeichert wird. Der Standardwert ist`FALSCH` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie Farben gerendert werden. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt diesen fest. Der Standardwert für diese Eigenschaft ist **leerer String** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in erzeugte Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Ermöglicht die Angabe des Rendering-Modus und der Qualität fürGraphics Objekt. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Ruft die horizontale Auflösung für die generierten Bilder in Punkten pro Zoll ab oder legt diese fest. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Ruft die Helligkeit für die generierten Bilder ab oder legt sie fest. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Ruft den Farbmodus für die generierten Bilder ab oder legt diesen fest. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Ruft den Kontrast für die generierten Bilder ab oder legt diesen fest. |
| [ImageSize](../../aspose.words.saving/imagesaveoptions/imagesize/) { get; set; } | Ruft die Größe eines generierten Bildes in Pixel ab oder legt diese fest. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der die Qualität der generierten JPEG-Bilder bestimmt. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Ermöglicht die Angabe, wie Metadateien in der gerenderten Ausgabe behandelt werden. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ruft ab oder legt fest[`NumeralFormat`](../numeralformat/) Wird zur Darstellung von Ziffern verwendet. Standardmäßig werden europäische Ziffern verwendet. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flag gibt an, ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist, werden redundante verschachtelte Leinwände und leere Leinwände entfernt, auch benachbarte Glyphen mit derselben Formatierung werden verkettet. Hinweis: Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden, wenn Diese Eigenschaft ist auf festgelegt`WAHR` . Standard ist`FALSCH` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie einzelne Seiten gespeichert werden, wenn ein Dokument in ein festes Seitenformat exportiert wird. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Ruft die zu rendernden Seiten ab oder legt diese fest. Standard sind alle Seiten im Dokument. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Ruft die Hintergrundfarbe (Papierfarbe) für die generierten Bilder ab oder legt diese fest. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Ruft das Pixelformat für die generierten Bilder ab oder legt es fest. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` hübsche Ausgabeformate, sofern zutreffend. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Legt sowohl die horizontale als auch die vertikale Auflösung für die generierten Bilder in Punkten pro Zoll fest. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem die gerenderten Dokumentseiten oder Formen gespeichert werden, wenn dieses Speicheroptionsobjekt verwendet wird. Kann ein Raster sein Tiff ,Png ,Bmp , Jpeg oder VektorEmf ,Eps , Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Ruft den Zoomfaktor für die generierten Bilder ab oder legt diesen fest. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, die beim Speichern in einer DOC- oder DOCX-Datei verwendet werden. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Ruft den Schwellenwert ab oder legt diesen fest, der den Wert des Binärisierungsfehlers in der Floyd-Steinberg-Methode bestimmt. wann[`ImageBinarizationMethod`](../imagebinarizationmethod/) IstFloydSteinbergDithering . |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Ruft die beim Konvertieren von Bildern in das 1-bpp-Format verwendete Methode ab oder legt diese fest. wann[`SaveFormat`](./saveformat/) IstTiff and [`TiffCompression`](./tiffcompression/) ist gleichCcitt3 oderCcitt4 . |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Ruft den Komprimierungstyp ab, der beim Speichern generierter Bilder im TIFF-Format angewendet werden soll, oder legt diesen fest. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Die Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Anti-Aliasing für das Rendering verwendet werden soll oder nicht. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob beim Speichern in EMF der Metadatei-Renderer GDI+ oder Aspose.Words verwendet werden soll. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Ruft die vertikale Auflösung für die generierten Bilder in Punkten pro Zoll ab oder legt diese fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Erstellt einen tiefen Klon dieses Objekts. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |

### Beispiele

Rendert eine Seite eines Word-Dokuments in ein Bild mit transparentem oder farbigem Hintergrund.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein „ImageSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft „PaperColor“ auf eine transparente Farbe, um eine transparente Farbe anzuwenden
// Hintergrund des Dokuments beim Rendern in ein Bild.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Setzen Sie die Eigenschaft „PaperColor“ auf eine undurchsichtige Farbe, um diese Farbe anzuwenden
// als Hintergrund des Dokuments, während wir es in ein Bild rendern.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Zeigt, wie die Komprimierung beim Speichern eines Dokuments als JPEG konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Erstellen Sie ein „ImageSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Setzen Sie die Eigenschaft „JpegQuality“ auf „10“, um beim Rendern des Dokuments eine stärkere Komprimierung zu verwenden.
// Dadurch wird die Dateigröße des Dokuments verringert, das Bild weist jedoch deutlichere Komprimierungsartefakte auf.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Setzen Sie die Eigenschaft „JpegQuality“ auf „100“, um beim Rendern des Dokuments eine schwächere Komprimierung zu verwenden.
// Dies verbessert die Qualität des Bildes auf Kosten einer größeren Dateigröße.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Zeigt, wie man beim Rendern eines Dokuments in PNG eine Auflösung angibt.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Erstellen Sie ein „ImageSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
            // um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Setzen Sie die Eigenschaft „Resolution“ auf „72“, um das Dokument mit 72 dpi darzustellen.
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
            // Setzen Sie die Eigenschaft „Resolution“ auf „300“, um das Dokument mit 300 dpi darzustellen.
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

### Siehe auch

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


