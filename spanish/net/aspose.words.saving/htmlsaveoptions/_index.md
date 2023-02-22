---
title: Class HtmlSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.HtmlSaveOptions clase. Se puede utilizar para especificar opciones adicionales al guardar un documento en elHtml  Mhtml oEpub formato.
type: docs
weight: 4850
url: /es/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elHtml , Mhtml oEpub formato.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elHtml formato. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(SaveFormat) | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elHtml ,Mhtml oEpub formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Especifica si las sangrías izquierda y derecha negativas de los párrafos se normalizan al guardar en HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Especifica un prefijo que se agrega a todos los nombres de clase CSS. El valor predeterminado es una cadena vacía y los nombres de clase CSS generados no tienen un prefijo común. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Permite controlar cómo se guardan los estilos CSS cuando un documento se guarda en HTML, MHTML o EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Especifica la ruta y el nombre del archivo de hoja de estilo en cascada (CSS) escrito cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Especifica cómo se exportan los estilos CSS (hoja de estilos en cascada) a HTML, MHTML o EPUB. El valor predeterminado esInline para HTML/MHTML y External para EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Permite controlar cómo se guardan las partes del documento cuando un documento se guarda en HTML o EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Especifica cómo se debe dividir el documento al guardar enHtml oEpub formato. El valor predeterminado esNone para HTML y HeadingParagraph para EPUB. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Especifica el nivel máximo de encabezados en los que dividir el documento. El valor predeterminado es`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Especifica la codificación que se utilizará al exportar a HTML, MHTML o EPUB. El valor predeterminado es`nueva codificación UTF8 (falso)` (UTF-8 sin lista de materiales). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/) { get; set; } | Especifica el nivel máximo de encabezados que se completan en el mapa de navegación cuando se exporta a formato IDPF EPUB. El valor predeterminado es`3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Especifica si se deben usar las URL de CID (Content-ID) para hacer referencia a los recursos (imágenes, fuentes, CSS) incluidos en los documentos MHTML . El valor predeterminado es`falso` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Especifica si exportar las propiedades del documento integradas y personalizadas a HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Controla cómo se guardan los campos del formulario desplegable en HTML o MHTML. El valor predeterminado es`falso` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Especifica si los recursos de fuentes se deben incrustar en HTML en codificación Base64. El valor predeterminado es`falso` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Especifica cómo se envían los encabezados y pies de página a HTML, MHTML o EPUB. El valor predeterminado esPerSection para HTML/MHTML yNone para EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Especifica si las imágenes se guardan en formato Base64 en la salida HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Especifica si la información de idioma se exporta a HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Controla cómo se envían las etiquetas de lista a HTML, MHTML o EPUB. El valor predeterminado esAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Especifica si se debe usar la URL original como la URL de las imágenes vinculadas. El valor predeterminado es`falso` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Especifica si los márgenes de la página se exportan a HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Especifica si la configuración de la página se exporta a HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Especifica si los tamaños de fuente se deben generar en unidades relativas al guardar en HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Especifica si se escribe la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es`verdadero` para HTML y`falso` para MHTML y EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Controla si[`Shape`](../../aspose.words.drawing/shape/) los nodos se convierten en imágenes SVG cuando se guardan en HTML, MHTML o EPUB. El valor predeterminado es`falso` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Controla cómo se guardan los campos de formulario de entrada de texto en HTML o MHTML. El valor predeterminado es`falso` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Especifica si se escriben números de página en la tabla de contenido al guardar HTML, MHTML y EPUB. El valor predeterminado es`falso` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Especifica si escribir la declaración DOCTYPE al guardar en HTML o MHTML. Cuando`verdadero` , escribe una declaración DOCTYPE en el documento anterior al elemento raíz. El valor predeterminado es`falso`. Al guardar en EPUB o HTML5 (Html5 ) siempre se escribe la declaración DOCTYPE . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Controla qué recursos de fuentes necesitan subconjuntos al guardar en HTML, MHTML o EPUB. El valor predeterminado es`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Permite controlar cómo se guardan las fuentes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir URI de fuentes escritas en un documento HTML. El valor predeterminado es una cadena vacía. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Especifica la versión del estándar HTML que debe utilizarse al guardar el documento en HTML o MHTML. El valor predeterminado esXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Especifica la resolución de salida de las imágenes cuando se exportan a HTML, MHTML o EPUB. El valor predeterminado es`96 ppp` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las imágenes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Especifica la carpeta física donde se guardan las imágenes al exportar un documento a formato HTML. El valor predeterminado es una cadena vacía. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir URI de imagen escritos en un documento HTML. El valor predeterminado es una cadena vacía. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Especifica en qué formato se guardan los metarchivos al exportar a HTML, MHTML o EPUB. El valor predeterminado esPng , lo que significa que los metarchivos se representan en imágenes PNG de trama. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Controla cómo se exportan los objetos de OfficeMath a HTML, MHTML o EPUB. El valor predeterminado es`HtmlOfficeMathOutputMode.Imagen` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Especifica si los nombres de familia de fuentes utilizados en el documento se resuelven y sustituyen de acuerdo con [`FontSettings`](../../aspose.words/document/fontsettings/) cuando se escribe en formatos basados en HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Especifica una carpeta física donde todos los recursos como imágenes, fuentes y CSS externo se guardan cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir URI de todos los recursos escritos en un documento HTML. El valor predeterminado es una cadena vacía. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serHtml ,Mhtml oEpub . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Especifica si Aspose.Words escala las imágenes al tamaño de la forma límite cuando se exportan a HTML, MHTML o EPUB. El valor predeterminado es`verdadero` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Controla cómo se exportan los anchos de tabla, fila y celda a HTML, MHTML o EPUB. El valor predeterminado esAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |

### Ejemplos

Muestra cómo especificar la carpeta para almacenar imágenes vinculadas después de guardarlas en .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Establecer una opción para exportar campos de formulario como texto sin formato en lugar de elementos de entrada HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Muestra cómo usar una codificación específica al guardar un documento en .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Use un objeto SaveOptions para especificar la codificación de un documento que guardaremos.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Por defecto, un documento de salida .epub tendrá todo su contenido en una parte HTML.
// Un criterio de división nos permite segmentar el documento en varias partes HTML.
// Estableceremos los criterios para dividir el documento en párrafos de encabezado.
// Esto es útil para lectores que no pueden leer archivos HTML más grandes que un tamaño específico.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Especificar que queremos exportar las propiedades del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Muestra cómo dividir un documento en partes y guardarlas.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crear un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si guardamos el documento normalmente, habrá un HTML de salida
    // documento con todo el contenido del documento fuente.
    // Establecer la propiedad "DocumentSplitCriteria" en "DocumentSplitCriteria.SectionBreak" para
    // guarda nuestro documento en varios archivos HTML: uno para cada sección.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Asigne una devolución de llamada personalizada a la propiedad "DocumentPartSavingCallback" para modificar la lógica de guardado de la parte del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si convertimos un documento que contiene imágenes en html, terminaremos con un archivo html que enlaza con varias imágenes.
    // Cada imagen tendrá la forma de un archivo en el sistema de archivos local.
    // También hay una devolución de llamada que puede personalizar el nombre y la ubicación del sistema de archivos de cada imagen.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Establece nombres de archivo personalizados para los documentos de salida en los que la operación de guardado divide un documento.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Podemos acceder a todo el documento de origen a través de la propiedad "Documento".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // A continuación hay dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establecer un nombre de archivo para el archivo de parte de salida:
        args.DocumentPartFileName = partFileName;

        // 2 - Cree una secuencia personalizada para el archivo de la parte de salida:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Establece nombres de archivo personalizados para los archivos de imagen que crea una conversión HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // A continuación hay dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establecer un nombre de archivo para el archivo de imagen de salida:
        args.ImageFileName = imageFileName;

        // 2 - Cree una secuencia personalizada para el archivo de imagen de salida:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Ver también

* class [SaveOptions](../saveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


