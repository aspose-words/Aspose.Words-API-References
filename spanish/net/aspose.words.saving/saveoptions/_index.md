---
title: SaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Esta es una clase base abstracta para clases que permiten al usuario especificar opciones adicionales al guardar un documento en un formato particular.
type: docs
weight: 5300
url: /es/net/aspose.words.saving/saveoptions/
---
## SaveOptions class

Esta es una clase base abstracta para clases que permiten al usuario especificar opciones adicionales al guardar un documento en un formato particular.

```csharp
public abstract class SaveOptions
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [CreateSaveOptions](../../aspose.words.saving/saveoptions/createsaveoptions#createsaveoptions)(SaveFormat) | Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado. |
| static [CreateSaveOptions](../../aspose.words.saving/saveoptions/createsaveoptions#createsaveoptions_1)(string) | Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado. |

### Observaciones

Una instancia de la clase SaveOptions o cualquier clase derivada se pasa a la secuencia[`Save`](../../aspose.words/document/save) o cadena[`Save`](../../aspose.words/document/save) sobrecargas para que el usuario defina opciones personalizadas al guardar un documento.

### Ejemplos

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

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
