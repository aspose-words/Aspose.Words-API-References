---
title: Class HtmlFixedSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.HtmlFixedSaveOptions clase. Se puede utilizar para especificar opciones adicionales al guardar un documento en elHtmlFixed formato.
type: docs
weight: 5080
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elHtmlFixed formato.

Para obtener más información, visite el[Especificar opciones de guardar](https://docs.aspose.com/words/net/specify-save-options/) artículo de documentación.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento una vez guardado. El valor predeterminado es`FALSO` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los colores. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Especifica el prefijo que se agrega a todos los nombres de clase en el archivo style.css. El valor predeterminado es`"ay"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Especifica la codificación que se utilizará al exportar a HTML. El valor predeterminado es`nueva codificación UTF8 (verdadero)` (UTF-8 con lista de materiales). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Especifica si el CSS (hoja de estilos en cascada) debe incrustarse en el documento HTML. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Especifica si las fuentes deben incrustarse en el documento HTML en formato Base64. Tenga en cuenta que configurar este indicador puede aumentar significativamente el tamaño del archivo HTML de salida. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Especifica si las imágenes deben incrustarse en un documento HTML en formato Base64. Tenga en cuenta que configurar este indicador puede aumentar significativamente el tamaño del archivo HTML de salida. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Especifica si los recursos SVG deben incrustarse en el documento HTML. El valor predeterminado es`verdadero` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Obtiene o establece una indicación de si los campos del formulario se exportan como elementos interactivos (como etiqueta de "entrada") en lugar de convertirse a texto o gráficos. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Obtiene o establece[`ExportFontFormat`](../exportfontformat/) utilizado para exportar fuentes. El valor predeterminado esWoff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permite especificar opciones de representación de metarchivos. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtiene o establece[`NumeralFormat`](../numeralformat/) se utiliza para representar números. Los números europeos se utilizan de forma predeterminada. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | El indicador indica si es necesario optimizar la salida. Si este indicador está configurado, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad está establecida en`verdadero` . El valor predeterminado es`verdadero` . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Especifica la alineación horizontal de las páginas en un documento HTML. El valor predeterminado esCenter . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Especifica los márgenes alrededor de las páginas en un documento HTML. El valor de los márgenes se mide en puntos y debe ser igual o mayor que 0. El valor predeterminado es 10 puntos. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a formato de página fija. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtiene o establece las páginas que se van a representar. El valor predeterminado son todas las páginas del documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` salida con bonitos formatos cuando corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Permite controlar cómo se guardan los recursos (imágenes, fuentes y css) cuando se exporta un documento a formato HTML de página fija. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Especifica la carpeta física donde se guardan los recursos (imágenes, fuentes, CSS) al exportar un documento al formato HTML. El valor predeterminado es`nulo` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir URI de imágenes escritas en un documento HTML. El valor predeterminado es`nulo` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | El indicador indica si las reglas CSS "@font-face" deben colocarse en un archivo separado "fontFaces.css" cuando un documento se guarda con una hoja de estilo externa (es decir, cuando[`ExportEmbeddedCss`](./exportembeddedcss/) es`FALSO` ). El valor predeterminado es`FALSO` , todas las reglas CSS se escriben en un único archivo "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo se puedeHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Especifica si se deben mostrar los bordes alrededor de las páginas. El valor predeterminado es`verdadero` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se utiliza o no el suavizado para la representación. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lentos). |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | El indicador indica si se deben usar fuentes de la máquina de destino para mostrar el documento. Si este indicador está configurado en`verdadero` ,[`FontFormat`](./fontformat/) y[`ExportEmbeddedFonts`](./exportembeddedfonts/) las propiedades no tienen efecto, también[`ResourceSavingCallback`](./resourcesavingcallback/) no se activa para las fuentes. El valor predeterminado es`FALSO` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Determina si el objeto especificado tiene el mismo valor que el objeto actual. |

### Ejemplos

Muestra cómo utilizar una devolución de llamada para imprimir los URI de recursos externos creados al convertir un documento a HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // Una carpeta especificada por ResourcesFolderAlias contendrá los recursos en lugar de ResourcesFolder.
    // Debemos asegurarnos de que la carpeta exista antes de que las transmisiones puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Cuenta e imprime los URI de los recursos contenidos en a medida que se convierten a HTML fijo.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Si configuramos un alias de carpeta en el objeto SaveOptions, podremos imprimirlo desde aquí.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // De forma predeterminada, 'ResourceFileUri' usa la carpeta del sistema para las fuentes.
                // Para evitar problemas en otras plataformas debes especificar explícitamente la ruta de las fuentes.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Si hemos especificado una carpeta en la propiedad "ResourcesFolderAlias",
        // también necesitaremos redirigir cada secuencia para colocar su recurso en esa carpeta.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Ver también

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


