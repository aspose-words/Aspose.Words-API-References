---
title: ImageSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Permet de spécifier des options supplémentaires lors du rendu des pages de document ou des formes en images.
type: docs
weight: 4970
url: /fr/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Permet de spécifier des options supplémentaires lors du rendu des pages de document ou des formes en images.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions)(SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer les images rendues dans the Tiff ,Png ,Bmp , Emf ,Jpeg ouSvg format. Png ,Bmp ,Jpeg ouSvg format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des couleurs. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions) { get; set; } | Permet de spécifier le mode et la qualité de rendu pour leGraphics objet. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution) { get; set; } | Obtient ou définit la résolution horizontale des images générées, en points par pouce. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness) { get; set; } | Obtient ou définit la luminosité des images générées. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode) { get; set; } | Obtient ou définit le mode de couleur pour les images générées. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast) { get; set; } | Obtient ou définit le contraste des images générées. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality) { get; set; } | Obtient ou définit une valeur déterminant la qualité des images JPEG générées. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions) { get; } | Permet de spécifier comment les métafichiers sont traités dans la sortie rendue. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Obtient ou définit[`NumeralFormat`](../numeralformat) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, également les glyphes voisins avec le même formatage sont concaténés. Remarque : La précision de l'affichage du contenu peut être affectée si cette propriété est définie sur true. La valeur par défaut est false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté au format de page fixe. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset) { get; set; } | Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor) { get; set; } | Obtient ou définit la couleur d'arrière-plan (papier) des images générées. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat) { get; set; } | Obtient ou définit le format de pixel pour les images générées. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution) { set; } | Définit à la fois la résolution horizontale et verticale des images générées, en points par pouce. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat) { get; set; } | Spécifie le format dans lequel les pages ou les formes du document rendu seront enregistrées si cet objet d'options d'enregistrement est utilisé. Peut être un raster Tiff ,Png ,Bmp , Jpeg ou vecteurEmf ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale) { get; set; } | Obtient ou définit le facteur de zoom pour les images générées. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering) { get; set; } | Obtient ou définit le seuil qui détermine la valeur de l'erreur de binarisation dans la méthode Floyd-Steinberg. lorsque[`ImageBinarizationMethod`](../imagebinarizationmethod) est ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod) { get; set; } | Obtient ou définit la méthode utilisée lors de la conversion des images au format 1 bpp lorsque[`SaveFormat`](./saveformat) est SaveFormat.Tiff and [`TiffCompression`](./tiffcompression) est égal à TiffCompression.Ccitt3 ou TiffCompression.Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression) { get; set; } | Obtient ou définit le type de compression à appliquer lors de l'enregistrement des images générées au format TIFF. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer) { get; set; } | Obtient ou définit une valeur déterminant s'il faut utiliser le rendu de métafichier GDI+ ou Aspose.Words lors de l'enregistrement au format EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution) { get; set; } | Obtient ou définit la résolution verticale des images générées, en points par pouce. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone)() | Crée un clone profond de cet objet. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

### Exemples

Rend une page d'un document Word en une image avec un arrière-plan transparent ou coloré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Crée un objet "ImageSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété "PaperColor" sur une couleur transparente pour appliquer un transparent
// arrière-plan du document lors de son rendu en image.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Définissez la propriété "PaperColor" sur une couleur opaque pour appliquer cette couleur
// comme arrière-plan du document tel que nous le rendons en image.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crée un objet "ImageSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Définissez la propriété "JpegQuality" sur "10" pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus importants.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Définissez la propriété "JpegQuality" sur "100" pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une taille de fichier accrue.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Montre comment spécifier une résolution lors du rendu d'un document au format PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Crée un objet "ImageSaveOptions" que nous pouvons passer à la méthode "Save" du document
            // pour modifier la façon dont cette méthode rend le document en image.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Définissez la propriété "Résolution" sur "72" pour rendre le document en 72dpi.
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
            // Définissez la propriété "Résolution" sur "300" pour afficher le document en 300 dpi.
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

### Voir également

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
