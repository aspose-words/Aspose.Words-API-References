---
title: MarkdownSaveOptions Class
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words para .NET
description: Descubre Aspose.Words.Saving.MarkdownSaveOptions para guardar documentos en formato Markdown de forma optimizada. ¡Personaliza tu resultado con opciones avanzadas hoy mismo!
type: docs
weight: 6060
url: /es/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Clase para especificar opciones adicionales al guardar un documento en elMarkdown formato.

Para obtener más información, visite el[Especificar opciones de guardado](https://docs.aspose.com/words/net/specify-save-options/) Artículo de documentación.

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elMarkdown formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe permitir la incrustación de fuentes con contornos PostScript al incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado es`FALSO` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha y hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [EmptyParagraphExportMode](../../aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/) { get; set; } | Especifica cómo exportar párrafos vacíos a Markdown. El valor predeterminado esEmptyLine . |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Especifica la codificación que se utilizará al exportar en formatos de texto. El valor predeterminado es**Codificación.UTF8** . |
| [ExportAsHtml](../../aspose.words.saving/markdownsaveoptions/exportashtml/) { get; set; } | Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar. El valor predeterminado esNone . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Especifica la forma en que se exportan los encabezados y pies de página a los formatos de texto. El valor predeterminado esPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Especifica si las imágenes se guardan en formato Base64 en el archivo de salida. El valor predeterminado es`FALSO` . |
| [ExportUnderlineFormatting](../../aspose.words.saving/markdownsaveoptions/exportunderlineformatting/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe exportar el formato de texto subrayado como una secuencia de dos caracteres más "++". El valor predeterminado es`FALSO` . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Permite especificar si los saltos de página deben conservarse durante la exportación. |
| [ImageResolution](../../aspose.words.saving/markdownsaveoptions/imageresolution/) { get; set; } | Especifica la resolución de salida de las imágenes al exportar a Markdown. El valor predeterminado es`96 ppp` . |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las imágenes cuando se guarda un documento en Markdown formato. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Especifica la carpeta física donde se guardan las imágenes al exportar un documento a Markdown Formato. El valor predeterminado es una cadena vacía. |
| [ImagesFolderAlias](../../aspose.words.saving/markdownsaveoptions/imagesfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir las URI de imágenes escritas en un documento. El valor predeterminado es una cadena vacía. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [LinkExportMode](../../aspose.words.saving/markdownsaveoptions/linkexportmode/) { get; set; } | Especifica cómo se escribirán los enlaces en el archivo de salida. El valor predeterminado esAuto . |
| [ListExportMode](../../aspose.words.saving/markdownsaveoptions/listexportmode/) { get; set; } | Especifica cómo se escribirán los elementos de la lista en el archivo de salida. El valor predeterminado esMarkdownSyntax . |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece un valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [OfficeMathExportMode](../../aspose.words.saving/markdownsaveoptions/officemathexportmode/) { get; set; } | Especifica cómo se escribirá OfficeMath en el archivo de salida. El valor predeterminado esText . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Especifica la cadena que se utilizará como salto de párrafo al exportar en formatos de texto. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Cuando`verdadero` , formatos bonitos de salida donde corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama al guardar un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Obtiene o establece un valor que especifica cómo alinear el contenido en las tablas al exportar a laMarkdown format. El valor predeterminado esAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté utilizando. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) La propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) La propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se debe utilizar o no suavizado para la representación. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se deben utilizar o no algoritmos de renderizado de alta calidad (es decir, lentos). |

## Ejemplos

Muestra cómo cambiar el nombre de la imagen al guardarla en un documento Markdown.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Si convertimos un documento que contiene imágenes a Markdown, terminaremos con un archivo Markdown que se vincula a varias imágenes.
    //Cada imagen tendrá la forma de un archivo en el sistema de archivos local.
    // También hay una devolución de llamada que puede personalizar el nombre y la ubicación del sistema de archivos de cada imagen.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // El método ImageSaving() de nuestra devolución de llamada se ejecutará en este momento.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Cambia el nombre de las imágenes guardadas que se producen cuando se guarda un documento Markdown.
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

        args.ImageFileName = imageFileName;
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

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
