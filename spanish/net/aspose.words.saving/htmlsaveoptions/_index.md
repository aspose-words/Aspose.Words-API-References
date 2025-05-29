---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Saving.HtmlSaveOptions para mejorar el guardado de documentos en formatos HTML, MHTML, EPUB, AZW3 y MOBI con opciones personalizables.
type: docs
weight: 5860
url: /es/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en el Html ,Mhtml ,Epub , Azw3 oMobi formato.

Para obtener más información, visite el[Especificar opciones de guardado](https://docs.aspose.com/words/net/specify-save-options/) Artículo de documentación.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elHtml formato. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elHtml ,Mhtml ,Epub , Azw3 oMobi formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe permitir la incrustación de fuentes con contornos PostScript al incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado es`FALSO` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Especifica si las sangrías negativas izquierda y derecha de los párrafos se normalizan al guardar en HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Especifica un prefijo que se agrega a todos los nombres de clase CSS. El valor predeterminado es una cadena vacía y los nombres de clase CSS generados no tienen un prefijo común. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Permite controlar cómo se guardan los estilos CSS cuando un documento se guarda en HTML, MHTML o EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Especifica la ruta y el nombre del archivo de hoja de estilo en cascada (CSS) que se escribe cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Especifica cómo se exportan los estilos CSS (hojas de estilo en cascada) a HTML, MHTML o EPUB. El valor predeterminado esInline para HTML/MHTML y External para EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha y hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Permite controlar cómo se guardan las partes del documento cuando un documento se guarda en HTML o EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Especifica cómo se debe dividir el documento al guardarlo enHtml , Epub oAzw3 format. El valor predeterminado esNone para HTML y HeadingParagraph para EPUB y AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Especifica el nivel máximo de encabezados en el que se dividirá el documento. El valor predeterminado es`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Especifica la codificación que se utilizará al exportar a HTML, MHTML o EPUB. El valor predeterminado es`nueva codificación UTF8 (falso)` (UTF-8 sin BOM). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Especifica si se deben usar URL con CID (Content-ID) para referenciar recursos (imágenes, fuentes, CSS) incluidos en documentos MHTML . El valor predeterminado es`FALSO` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Especifica si se deben exportar las propiedades del documento personalizadas e integradas a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Controla cómo se guardan los campos del formulario desplegable en HTML o MHTML. El valor predeterminado es`FALSO` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Especifica si los recursos de fuentes deben incrustarse en HTML en codificación Base64. El valor predeterminado es`FALSO` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Especifica cómo se envían los encabezados y pies de página a HTML, MHTML o EPUB. El valor predeterminado esPerSection para HTML/MHTML yNone para EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Especifica si las imágenes se guardan en formato Base64 en la salida HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Especifica si la información del idioma se exporta a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Controla cómo se envían las etiquetas de lista a HTML, MHTML o EPUB. El valor predeterminado esAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Especifica si se debe utilizar la URL original como URL de las imágenes vinculadas. El valor predeterminado es`FALSO` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Especifica si los márgenes de la página se exportan a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Especifica si la configuración de página se exporta a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Especifica si los tamaños de fuente deben imprimirse en unidades relativas al guardar en HTML, MHTML o EPUB. El valor predeterminado es`FALSO` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Especifica si se debe escribir la información de ida y vuelta al guardar en HTML, MHTML o EPUB. El valor predeterminado es`verdadero` para HTML y`FALSO` para MHTML y EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Controla si[`Shape`](../../aspose.words.drawing/shape/)Los nodos se convierten en imágenes SVG al guardar en HTML, MHTML, EPUB o AZW3. El valor predeterminado es`FALSO` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Controla cómo se guardan los campos del formulario de entrada de texto en HTML o MHTML. El valor predeterminado es`FALSO` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Especifica si se deben escribir números de página en la tabla de contenido al guardar HTML, MHTML y EPUB. El valor predeterminado es`FALSO` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Especifica si se debe escribir la declaración DOCTYPE al guardar en HTML o MHTML. Cuando`verdadero` , escribe una declaración DOCTYPE en el documento antes del elemento raíz. El valor predeterminado es`FALSO`. Al guardar en EPUB o HTML5 (Html5 ) la declaración DOCTYPE siempre se escribe. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Controla qué recursos de fuente necesitan subconjunto al guardar en HTML, MHTML o EPUB. El valor predeterminado es`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Permite controlar cómo se guardan las fuentes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir las URI de fuentes escritas en un documento HTML. El valor predeterminado es una cadena vacía. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Especifica la versión del estándar HTML que se debe utilizar al guardar el documento en HTML o MHTML. El valor predeterminado esXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Especifica la resolución de salida de las imágenes al exportar a HTML, MHTML o EPUB. El valor predeterminado es`96 ppp` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las imágenes cuando un documento se guarda en HTML, MHTML o EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato HTML. El valor predeterminado es una cadena vacía. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir las URI de imágenes escritas en un documento HTML. El valor predeterminado es una cadena vacía. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece un valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Especifica en qué formato se guardan los metarchivos al exportar a HTML, MHTML o EPUB. El valor predeterminado esPng , lo que significa que los metarchivos se procesan en imágenes PNG rasterizadas. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | Especifica el nivel máximo de encabezados que se pueden rellenar en el mapa de navegación al exportar a los formatos EPUB, MOBI o AZW3 . El valor predeterminado es`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Controla cómo se exportan los objetos de OfficeMath a HTML, MHTML o EPUB. El valor predeterminado esImage . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Cuando`verdadero` , formatos bonitos de salida donde corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama al guardar un documento y acepta datos sobre el progreso del guardado. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/) { get; set; } | Especifica si se eliminará JavaScript de los enlaces. El valor predeterminado es`FALSO` . |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/) { get; set; } | Especifica si los caracteres de barra invertida deben reemplazarse con signos de yen. El valor predeterminado es`FALSO` . |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Especifica si los nombres de familias de fuentes utilizados en el documento se resuelven y sustituyen según [`FontSettings`](../../aspose.words/document/fontsettings/) al escribirse en formatos basados en HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Especifica una carpeta física donde se guardan todos los recursos, como imágenes, fuentes y CSS externo, al exportar un documento a HTML. El valor predeterminado es una cadena vacía. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir las URI de todos los recursos escritos en un documento HTML. El valor predeterminado es una cadena vacía. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serHtml ,Mhtml ,Epub , Azw3 oMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Especifica si Aspose.Words escala las imágenes al tamaño de la forma delimitadora al exportar a HTML, MHTML o EPUB. El valor predeterminado es`verdadero` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Controla cómo se exportan los anchos de tabla, fila y celda a HTML, MHTML o EPUB. El valor predeterminado esAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté utilizando. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) La propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) La propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se debe utilizar o no suavizado para la representación. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se deben utilizar o no algoritmos de renderizado de alta calidad (es decir, lentos). |

## Ejemplos

Muestra cómo especificar la carpeta para almacenar las imágenes vinculadas después de guardarlas en .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Establezca una opción para exportar los campos de formulario como texto simple en lugar de elementos de entrada HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Muestra cómo utilizar una codificación específica al guardar un documento en .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilice un objeto SaveOptions para especificar la codificación de un documento que guardaremos.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// De forma predeterminada, un documento .epub de salida tendrá todo su contenido en una parte HTML.
// Un criterio de división nos permite segmentar el documento en varias partes HTML.
// Estableceremos los criterios para dividir el documento en párrafos de encabezado.
// Esto es útil para los lectores que no pueden leer archivos HTML más grandes que un tamaño específico.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Especificamos que queremos exportar las propiedades del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Muestra cómo dividir un documento en partes y guardarlas.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crea un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si guardamos el documento normalmente, habrá un HTML de salida
    // documento con todo el contenido del documento fuente.
    // Establezca la propiedad "DocumentSplitCriteria" en "DocumentSplitCriteria.SectionBreak" en
    // guardamos nuestro documento en múltiples archivos HTML: uno para cada sección.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Asigne una devolución de llamada personalizada a la propiedad "DocumentPartSavingCallback" para alterar la lógica de guardado de partes del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si convertimos un documento que contiene imágenes a html, terminaremos con un archivo html que enlaza a varias imágenes.
    //Cada imagen tendrá la forma de un archivo en el sistema de archivos local.
    // También hay una devolución de llamada que puede personalizar el nombre y la ubicación del sistema de archivos de cada imagen.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Establece nombres de archivos personalizados para los documentos de salida en los que la operación de guardado divide un documento.
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
        //Podemos acceder al documento fuente completo a través de la propiedad "Documento".
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

        A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establezca un nombre de archivo para el archivo de la parte de salida:
        args.DocumentPartFileName = partFileName;

        // 2 - Crea una secuencia personalizada para el archivo de la parte de salida:
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

        A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establezca un nombre de archivo para el archivo de imagen de salida:
        args.ImageFileName = imageFileName;

        // 2 - Crea una secuencia personalizada para el archivo de imagen de salida:
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
