---
title: Class PdfSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfSaveOptions clase. Se puede utilizar para especificar opciones adicionales al guardar un documento en elPdf formato.
type: docs
weight: 5520
url: /es/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elPdf formato.

Para obtener más información, visite el[Especificar opciones de guardar](https://docs.aspose.com/words/net/specify-save-options/) artículo de documentación.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en Pdf formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Un indicador que especifica si se escriben operadores de posicionamiento de texto adicionales o no. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento una vez guardado. El valor predeterminado es`FALSO` . |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Obtiene o establece un valor que determina si se deben almacenar en caché los gráficos colocados en el fondo del documento. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los colores. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Especifica el nivel de cumplimiento de los estándares PDF para los documentos de salida. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Especifica si se deben convertir las referencias de notas al pie/notas al final en la historia del texto principal en hipervínculos activos. Cuando se hace clic en el hipervínculo, se dirigirá a la nota al pie/nota al final correspondiente. El valor predeterminado es`FALSO` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Obtiene o establece un valor que determina la forma[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) se exportan a un archivo PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Obtiene o establece los detalles para firmar el documento PDF de salida. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Un indicador que especifica si la barra de título de la ventana debe mostrar el título del documento tomado de la entrada Título del diccionario de información del documento. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Permite especificar opciones de reducción de resolución. |
| [EmbedAttachments](../../aspose.words.saving/pdfsaveoptions/embedattachments/) { get; set; } | Obtiene o establece un valor que determina si se incrustan o no archivos adjuntos en el documento PDF. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Controla cómo se incrustan las fuentes en los documentos PDF resultantes. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Obtiene o establece los detalles para cifrar el documento PDF de salida. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Obtiene o establece un valor que determina si se exporta o no la estructura del documento. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Obtiene o establece un valor que determina si se crea o no una etiqueta "Span" en la estructura del documento para exportar el idioma del texto. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Obtiene o establece un valor que determina si un gráfico de párrafo debe marcarse como un artefacto. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Especifica el modo de incrustación de fuente. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Determina cómo se exportan los marcadores en encabezados/pies de página. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Especifica el tipo de compresión que se utilizará para todas las imágenes del documento. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Un indicador que indica si la interpolación de imágenes debe ser realizada por un lector conforme. Cuando`FALSO` se especifica, la bandera no se escribe en el documento de salida y se utiliza en su lugar el comportamiento predeterminado del lector. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permite especificar opciones de representación de metarchivos. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtiene o establece[`NumeralFormat`](../numeralformat/) se utiliza para representar números. Los números europeos se utilizan de forma predeterminada. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Obtiene o establece un valor que determina si los hipervínculos en el documento PDF de salida se fuerzan a abrirse en una nueva ventana (o pestaña) de un navegador. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | El indicador indica si es necesario optimizar la salida. Si este indicador se establece en lienzos anidados redundantes y se eliminan los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad está establecida en`verdadero` . El valor predeterminado es`FALSO` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Permite especificar opciones de contorno. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Especifica cómo se debe mostrar el documento PDF cuando se abre en el lector de PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a formato de página fija. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtiene o establece las páginas que se van a representar. El valor predeterminado son todas las páginas del documento. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Obtiene o establece un valor que determina si se deben precombinar imágenes transparentes con color de fondo negro. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Especifica si se deben conservar los campos de formulario de Microsoft Word como campos de formulario en PDF o convertirlos a texto. El valor predeterminado es`FALSO` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` salida con bonitos formatos cuando corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo se puedePdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Especifica el tipo de compresión que se utilizará para todo el contenido textual del documento. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se utiliza o no el suavizado para la representación. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Obtiene o establece un valor que determina si se sustituyen o no las fuentes TrueType Arial, Times New Roman, Courier New y Symbol con fuentes PDF Type 1 principales. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lentos). |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Obtiene o establece un valor que determina qué tipo de zoom se debe aplicar cuando se abre un documento con un visor de PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Obtiene o establece un valor que determina el factor de zoom (en porcentajes) para un documento. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Crea un clon profundo de este objeto. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Determina si el objeto especificado tiene el mismo valor que el objeto actual. |

### Ejemplos

Muestra cómo cambiar el color de la imagen con la propiedad de opciones de guardado.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
// Establece la propiedad "ColorMode" en "Escala de grises" para representar todas las imágenes del documento en blanco y negro.
// El tamaño del documento de salida puede ser mayor con esta configuración.
// Establece la propiedad "ColorMode" en "Normal" para representar todas las imágenes en color.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Muestra cómo aplicar compresión de texto al guardar un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "TextCompression" en "PdfTextCompression.None" para no aplicar ninguna
// compresión a texto cuando guardamos el documento en PDF.
// Establece la propiedad "TextCompression" en "PdfTextCompression.Flate" para aplicar compresión ZIP
// al texto cuando guardamos el documento en PDF. Cuanto más grande sea el documento, mayor será el impacto que esto tendrá.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar títulos de los niveles 1 al 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los títulos en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su respectivo encabezado.
// Establece la propiedad "HeadingsOutlineLevels" en "4" para excluir del esquema todos los encabezados cuyos niveles estén por encima de 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si una entrada de esquema tiene entradas posteriores de un nivel superior entre ella y la siguiente entrada del mismo nivel o de un nivel inferior,
// aparecerá una flecha a la izquierda de la entrada. Esta entrada es la "propietaria" de varias de estas "subentradas".
// En nuestro documento, las entradas de esquema del quinto nivel de encabezado son subentradas de la segunda entrada de esquema del cuarto nivel,
// las entradas de nivel de título 4.º y 5.º son subentradas de la segunda entrada de 3.º nivel, y así sucesivamente.
// En el esquema, podemos hacer clic en la flecha de la entrada "propietario" para contraer/expandir todas sus subentradas.
// Establece la propiedad "ExpandedOutlineLevels" en "2" para expandir automáticamente todas las entradas de encabezado de nivel 2 e inferiores
// y colapsar todas las entradas de nivel 3 y superiores cuando abrimos el documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ver también

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


