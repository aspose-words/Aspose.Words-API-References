---
title: PdfSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Se puede utilizar para especificar opciones adicionales al guardar un documento en elPdf formato.
type: docs
weight: 5240
url: /es/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elPdf formato.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en el Pdf formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Un indicador que especifica si escribir o no operadores de posicionamiento de texto adicionales. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los colores. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Especifica el nivel de cumplimiento de estándares de PDF para los documentos de salida. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Especifica si convertir las referencias a notas al pie/notas al final en la historia del texto principal en hipervínculos activos. Al hacer clic en el hipervínculo, se llevará a la nota al pie/nota al final correspondiente. El valor predeterminado es`falso` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Obtiene o establece un valor que determina el camino[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) se exportan a archivo PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Obtiene o establece los detalles para firmar el documento PDF de salida. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Un indicador que especifica si la barra de título de la ventana debe mostrar el título del documento tomado de la entrada Título del diccionario de información del documento. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Permite especificar opciones de reducción de resolución. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Controla cómo se incrustan las fuentes en los documentos PDF resultantes. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Obtiene o establece los detalles para cifrar el documento PDF de salida. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Obtiene o establece un valor que determina si se exporta o no la estructura del documento. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Obtiene o establece un valor que determina si se crea o no una etiqueta "Span" en la estructura del documento para exportar el idioma del texto. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Especifica el modo de incrustación de fuentes. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Determina cómo se exportan los marcadores en encabezados/pies de página. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Especifica cómo se seleccionará el espacio de color para las imágenes en el documento PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Especifica el tipo de compresión que se utilizará para todas las imágenes del documento. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Un indicador que indica si la interpolación de imágenes debe ser realizada por un lector conforme. Cuando`falso` se especifica, el indicador no se escribe en el documento de salida y se usa el comportamiento predeterminado del lector en su lugar. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permite especificar las opciones de representación del metarchivo. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtiene o establece[`NumeralFormat`](../numeralformat/) se utiliza para representar números. Los números europeos se utilizan de forma predeterminada. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Obtiene o establece un valor que determina si los hipervínculos en el documento PDF de salida deben abrirse en una nueva ventana (o pestaña) de un navegador. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | El indicador indica si es necesario optimizar la salida. Si este indicador se establece, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en verdadero. El valor predeterminado es falso. |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Permite especificar opciones de contorno. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Especifica cómo se debe mostrar el documento PDF cuando se abre en el lector de PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a un formato de página fijo. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtiene o establece las páginas a representar. El valor predeterminado es todas las páginas del documento. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Obtiene o establece un valor que determina si se combinan o no las imágenes transparentes con el color de fondo negro. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Especifica si se conservarán los campos de formulario de Microsoft Word como campos de formulario en PDF o si se convertirán en texto. El valor predeterminado es`falso` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Especifica el tipo de compresión que se utilizará para todo el contenido textual del documento. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Obtiene o establece un valor booleano que indica si el documento debe guardarse utilizando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Obtiene o establece un valor que determina si se sustituyen o no las fuentes TrueType Arial, Times New Roman, Courier New y Symbol con fuentes principales PDF Type 1. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |
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
// Establezca la propiedad "Modo de color" en "Escala de grises" para representar todas las imágenes del documento en blanco y negro.
// El tamaño del documento de salida puede ser mayor con esta configuración.
// Establezca la propiedad "ColorMode" en "Normal" para representar todas las imágenes en color.
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

// Establecer la propiedad "TextCompression" en "PdfTextCompression.None" para no aplicar ninguna
// compresión a texto cuando guardamos el documento en PDF.
// Establecer la propiedad "TextCompression" en "PdfTextCompression.Flate" para aplicar la compresión ZIP
// a texto cuando guardamos el documento en PDF. Cuanto más grande sea el documento, mayor será el impacto que tendrá.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar encabezados de niveles 1 a 5.
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

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su respectivo encabezado.
// Establezca la propiedad "HeadingsOutlineLevels" en "4" para excluir todos los encabezados cuyos niveles estén por encima de 4 del esquema.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si una entrada de esquema tiene entradas posteriores de un nivel superior entre ella y la siguiente entrada del mismo nivel o inferior,
// aparecerá una flecha a la izquierda de la entrada. Esta entrada es el "propietario" de varias de estas "subentradas".
// En nuestro documento, las entradas de esquema del 5.º nivel de encabezado son subentradas de la segunda entrada de esquema del 4.º nivel,
  // las entradas de nivel de encabezado 4 y 5 son subentradas de la segunda entrada de nivel 3, y así sucesivamente.
// En el esquema, podemos hacer clic en la flecha de la entrada "propietario" para colapsar/expandir todas sus subentradas.
// Establezca la propiedad "ExpandedOutlineLevels" en "2" para expandir automáticamente todas las entradas de encabezado de nivel 2 e inferior
 // y colapsar todas las entradas de nivel y 3 y superiores cuando abrimos el documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Ver también

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
