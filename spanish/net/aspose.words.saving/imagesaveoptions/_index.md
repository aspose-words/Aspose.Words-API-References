---
title: ImageSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Permite especificar opciones adicionales al representar páginas de documentos o formas en imágenes.
type: docs
weight: 4970
url: /es/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

Permite especificar opciones adicionales al representar páginas de documentos o formas en imágenes.

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(SaveFormat) | Inicializa una nueva instancia de esta clase que se puede usar para guardar imágenes renderizadas en el Tiff ,Png ,Bmp , Emf ,Jpeg oSvg formato. Png ,Bmp ,Jpeg oSvg formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los colores. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | Permite especificar el modo de renderizado y la calidad para elGraphics objeto. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | Obtiene o establece la resolución horizontal de las imágenes generadas, en puntos por pulgada. |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | Obtiene o establece el brillo de las imágenes generadas. |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | Obtiene o establece el modo de color de las imágenes generadas. |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | Obtiene o establece el contraste de las imágenes generadas. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | Obtiene o establece un valor que determina la calidad de las imágenes JPEG generadas. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | Permite especificar cómo se tratan los metarchivos en la salida renderizada. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtiene o establece[`NumeralFormat`](../numeralformat/) se utiliza para representar números. Los números europeos se utilizan de forma predeterminada. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | El indicador indica si es necesario optimizar la salida. Si este indicador se establece, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en verdadero. El valor predeterminado es falso. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a un formato de página fijo. |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | Obtiene o establece las páginas a representar. El valor predeterminado es todas las páginas del documento. |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | Obtiene o establece el color de fondo (papel) de las imágenes generadas. |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | Obtiene o establece el formato de píxeles de las imágenes generadas. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | Establece la resolución horizontal y vertical de las imágenes generadas, en puntos por pulgada. |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardarán las formas o las páginas del documento renderizado si se usa este objeto de opciones de guardado. Puede ser un raster Tiff ,Png ,Bmp , Jpeg o vectorialEmf ,Svg . |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | Obtiene o establece el factor de zoom para las imágenes generadas. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | Obtiene o establece el umbral que determina el valor del error de binarización en el método Floyd-Steinberg. cuando[`ImageBinarizationMethod`](../imagebinarizationmethod/) es ImageBinarizationMethod.FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | Obtiene o establece el método utilizado al convertir imágenes a formato de 1 bpp cuando[`SaveFormat`](./saveformat/) es SaveFormat.Tiff y [`TiffCompression`](./tiffcompression/) es igual a TiffCompression.Ccitt3 o TiffCompression.Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | Obtiene o establece el tipo de compresión que se aplicará al guardar las imágenes generadas en formato TIFF. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | Obtiene o establece un valor que determina si usar GDI+ o el procesador de metarchivos Aspose.Words al guardar en EMF. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | Obtiene o establece la resolución vertical de las imágenes generadas, en puntos por pulgada. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | Crea un clon profundo de este objeto. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Determina si el objeto especificado tiene el mismo valor que el objeto actual. |

### Ejemplos

Convierte una página de un documento de Word en una imagen con fondo transparente o de color.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Establecer la propiedad "PaperColor" en un color transparente para aplicar un color transparente
// fondo del documento mientras se representa en una imagen.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Establecer la propiedad "PaperColor" en un color opaco para aplicar ese color
// como fondo del documento a medida que lo representamos en una imagen.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

Muestra cómo configurar la compresión al guardar un documento como JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Establezca la propiedad "JpegQuality" en "10" para usar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más prominentes.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Establezca la propiedad "JpegQuality" en "100" para usar una compresión más débil al procesar el documento.
// Esto mejorará la calidad de la imagen a costa de aumentar el tamaño del archivo.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

Muestra cómo especificar una resolución al renderizar un documento a PNG.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.Font.Name = "Times New Roman";
            builder.Font.Size = 24;
            builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

            builder.InsertImage(ImageDir + "Logo.jpg");

            // Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
            // para modificar la forma en que ese método convierte el documento en una imagen.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

            // Establezca la propiedad "Resolución" en "72" para representar el documento en 72 ppp.
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
            // Establezca la propiedad "Resolución" en "300" para representar el documento en 300 ppp.
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

### Ver también

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
