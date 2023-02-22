---
title: Class ImageSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.ImageSaveOptions classe. Consente di specificare opzioni aggiuntive durante il rendering di pagine o forme del documento in immagini.
type: docs
weight: 4970
url: /it/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Consente di specificare opzioni aggiuntive durante il rendering di pagine o forme del documento in immagini.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare le immagini renderizzate in Tiff ,Png ,Bmp , Emf ,Jpeg oSvg formato. Png ,Bmp ,Jpeg oSvg formato. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei colori. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Se true, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **VERO** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Consente di specificare la modalità di rendering e la qualità per ilGraphics oggetto. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Ottiene o imposta la risoluzione orizzontale per le immagini generate, in punti per pollice. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Ottiene o imposta la luminosità per le immagini generate. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Ottiene o imposta la modalità colore per le immagini generate. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Ottiene o imposta il contrasto per le immagini generate. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML). |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG generate. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se eseguire l'ottimizzazione della memoria prima di salvare il documento. Il valore predefinito per questa proprietà è **falso** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Consente di specificare come vengono trattati i metafile nell'output renderizzato. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat/) utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere compromessa se questa proprietà è impostata su true. L'impostazione predefinita è false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le pagine separate quando un documento viene esportato in un formato pagina fisso. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Ottiene o imposta le pagine di cui eseguire il rendering. Il valore predefinito è tutte le pagine nel documento. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Ottiene o imposta il colore di sfondo (carta) per le immagini generate. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Ottiene o imposta il formato pixel per le immagini generate. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formati graziosi di output ove applicabile. Il valore predefinito è **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Imposta la risoluzione orizzontale e verticale per le immagini generate, in punti per pollice. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Specifica il formato in cui verranno salvate le pagine o le forme del documento renderizzate se viene utilizzato questo oggetto delle opzioni di salvataggio. Può essere un raster Tiff ,Png ,Bmp , Jpeg o vettoreEmf ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Ottiene o imposta il fattore di zoom per le immagini generate. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Ottiene o imposta la soglia che determina il valore dell'errore di binarizzazione nel metodo Floyd-Steinberg. quando[`ImageBinarizationMethod`](../imagebinarizationmethod/) is ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Ottiene o imposta il metodo utilizzato durante la conversione delle immagini in formato 1 bpp quando[`SaveFormat`](./saveformat/) è SaveFormat.Tiff e [`TiffCompression`](./tiffcompression/) è uguale a TiffCompression.Ccitt3 o TiffCompression.Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Ottiene o imposta il tipo di compressione da applicare quando si salvano le immagini generate nel formato TIFF. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è **VERO** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) viene aggiornato prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-alias per il rendering. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare il renderer di metafile GDI+ o Aspose.Words durante il salvataggio in EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (cioè lenti). |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Ottiene o imposta la risoluzione verticale per le immagini generate, in punti per pollice. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Crea un clone profondo di questo oggetto. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |

### Esempi

Rendering di una pagina di un documento di Word in un'immagine con sfondo trasparente o colorato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Imposta la proprietà "PaperColor" su un colore trasparente per applicare un colore trasparente
// sfondo del documento durante il rendering in un'immagine.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Imposta la proprietà "PaperColor" su un colore opaco per applicare quel colore
// come sfondo del documento durante il rendering in un'immagine.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Mostra come configurare la compressione durante il salvataggio di un documento come JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Imposta la proprietà "JpegQuality" su "10" per utilizzare una compressione più forte durante il rendering del documento.
// Ciò ridurrà le dimensioni del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Imposta la proprietà "JpegQuality" su "100" per utilizzare una compressione più debole durante il rendering del documento.
// Ciò migliorerà la qualità dell'immagine al costo di una maggiore dimensione del file.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Mostra come specificare una risoluzione durante il rendering di un documento in formato PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
            // per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Imposta la proprietà "Risoluzione" su "72" per eseguire il rendering del documento a 72 dpi.
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
            // Imposta la proprietà "Risoluzione" su "300" per eseguire il rendering del documento a 300 dpi.
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

### Guarda anche

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


