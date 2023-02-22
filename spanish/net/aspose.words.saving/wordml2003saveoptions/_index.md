---
title: Class WordML2003SaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.WordML2003SaveOptions clase. Se puede utilizar para especificar opciones adicionales al guardar un documento en elWordML formato.
type: docs
weight: 5400
url: /es/net/aspose.words.saving/wordml2003saveoptions/
---
## WordML2003SaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elWordML formato.

```csharp
public class WordML2003SaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [WordML2003SaveOptions](wordml2003saveoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/wordml2003saveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeWordML . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |

### Observaciones

Por el momento proporciona sólo el[`SaveFormat`](./saveformat/) propiedad, pero en el futuro pueden tener otras opciones añadidas.

### Ejemplos

Muestra cómo administrar la optimización de la memoria.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crear un objeto "WordML2003SaveOptions" para pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en el formato de guardado de WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

// Establezca el indicador "MemoryOptimization" en "true" para disminuir el consumo de memoria
// durante la operación de guardado del documento a costa de un mayor tiempo de guardado.
// Establezca el indicador "MemoryOptimization" en "falso" para guardar el documento normalmente.
options.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.MemoryOptimization.xml", options);
```

Muestra cómo administrar el contenido sin procesar del documento de salida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crear un objeto "WordML2003SaveOptions" para pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en el formato de guardado de WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// Establezca la propiedad "PrettyFormat" en "true" para aplicar la sangría de caracteres de tabulación y
// saltos de línea para facilitar la lectura del contenido sin procesar del documento de salida.
// Establezca la propiedad "PrettyFormat" en "falso" para guardar el contenido sin procesar del documento en un cuerpo continuo del texto.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");

if (prettyFormat)
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties>\r\n\t\t" +
            "<o:Revision>1</o:Revision>\r\n\t\t" +
            "<o:TotalTime>0</o:TotalTime>\r\n\t\t" +
            "<o:Pages>1</o:Pages>\r\n\t\t" +
            "<o:Words>0</o:Words>\r\n\t\t" +
            "<o:Characters>0</o:Characters>\r\n\t\t" +
            "<o:Lines>1</o:Lines>\r\n\t\t" +
            "<o:Paragraphs>1</o:Paragraphs>\r\n\t\t" +
            "<o:CharactersWithSpaces>0</o:CharactersWithSpaces>\r\n\t\t" +
            "<o:Version>11.5606</o:Version>\r\n\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### Ver también

* class [SaveOptions](../saveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


