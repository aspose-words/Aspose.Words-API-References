---
title: XamlFixedSaveOptions Class
linktitle: XamlFixedSaveOptions
articleTitle: XamlFixedSaveOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.Saving.XamlFixedSaveOptions para guardar documentos en formato XamlFixed de forma optimizada. ¡Desbloquee funciones avanzadas para obtener resultados superiores!
type: docs
weight: 6490
url: /es/net/aspose.words.saving/xamlfixedsaveoptions/
---
## XamlFixedSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elXamlFixed formato.

Para obtener más información, visite el[Especificar opciones de guardado](https://docs.aspose.com/words/net/specify-save-options/) Artículo de documentación.

```csharp
public class XamlFixedSaveOptions : FixedPageSaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [XamlFixedSaveOptions](xamlfixedsaveoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe permitir la incrustación de fuentes con contornos PostScript al incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado es`FALSO` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los colores. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha y hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Obtiene o establece un valor que determina la calidad de las imágenes JPEG dentro del documento HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece un valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permite especificar opciones de representación de metarchivos. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtiene o establece[`NumeralFormat`](../numeralformat/) Se utiliza para la representación de números. Los números europeos se utilizan de forma predeterminada. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | El indicador indica si es necesario optimizar la salida. Si se establece este indicador, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en`verdadero` . El valor predeterminado es`FALSO` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permite controlar cómo se guardan las páginas separadas cuando un documento se exporta a un formato de página fijo. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtiene o establece las páginas que se representarán. El valor predeterminado son todas las páginas del documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Cuando`verdadero` , formatos bonitos de salida donde corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama al guardar un documento y acepta datos sobre el progreso del guardado. |
| [ResourceSavingCallback](../../aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Permite controlar cómo se guardan los recursos (imágenes y fuentes) cuando un documento se exporta al formato Xaml de página fija. |
| [ResourcesFolder](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/) { get; set; } | Especifica la carpeta física donde se guardan los recursos (imágenes y fuentes) al exportar un documento al formato Xaml de página fija. El valor predeterminado es`nulo` . |
| [ResourcesFolderAlias](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Especifica el nombre de la carpeta utilizada para construir las URI de imágenes escritas en un documento Xaml de página fija. El valor predeterminado es`nulo` . |
| override [SaveFormat](../../aspose.words.saving/xamlfixedsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeXamlFixed . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté utilizando. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) La propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) La propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se debe utilizar o no suavizado para la representación. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se deben utilizar o no algoritmos de renderizado de alta calidad (es decir, lentos). |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |

## Ejemplos

Muestra cómo imprimir las URI de los recursos vinculados creados al convertir un documento a formato fijo .xaml.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crea un objeto "XamlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que guardamos el documento en el formato de guardado XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilice la propiedad "ResourcesFolder" para asignar una carpeta en el sistema de archivos local a la que
    // Aspose.Words guardará todos los recursos vinculados del documento, como imágenes y fuentes.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilice la propiedad "ResourcesFolderAlias" para usar esta carpeta
    // al construir URI de imágenes en lugar del nombre de la carpeta de recursos.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Una carpeta especificada por "ResourcesFolderAlias" deberá contener los recursos en lugar de "ResourcesFolder".
    // Debemos asegurarnos de que la carpeta exista antes de que los flujos de devolución de llamada puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Cuenta e imprime las URI de los recursos creados durante la conversión a .xaml fijo.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Si especificamos un alias de carpeta de recursos, también necesitaríamos
        // para redirigir cada flujo para colocar su recurso en la carpeta alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Ver también

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
