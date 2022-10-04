---
title: TxtSaveOptionsBase
second_title: Referencia de API de Aspose.Words para .NET
description: La clase base para especificar opciones adicionales al guardar un documento en formatos basados en texto.
type: docs
weight: 5390
url: /es/net/aspose.words.saving/txtsaveoptionsbase/
---
## TxtSaveOptionsBase class

La clase base para especificar opciones adicionales al guardar un documento en formatos basados en texto.

```csharp
public abstract class TxtSaveOptionsBase : SaveOptions
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Especifica la codificación que se utilizará al exportar en formatos de texto. El valor predeterminado es **Codificación.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Especifica la forma en que se exportan los encabezados y pies de página a los formatos de texto. El valor predeterminado esPrimaryOnly . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Permite especificar si los saltos de página deben conservarse durante la exportación. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Especifica la cadena que se utilizará como salto de párrafo al exportar en formatos de texto. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |

### Ejemplos

Muestra cómo guardar un documento .txt con un salto de párrafo personalizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Crear un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en texto sin formato.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Establecer "ParagraphBreak" en un valor personalizado que deseamos poner al final de cada párrafo.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Ver también

* class [SaveOptions](../saveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
