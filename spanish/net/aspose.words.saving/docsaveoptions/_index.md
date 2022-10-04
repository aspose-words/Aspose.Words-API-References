---
title: DocSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Se puede utilizar para especificar opciones adicionales al guardar un documento en elDoc or Dot formato.
type: docs
weight: 4670
url: /es/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elDoc or Dot formato.

```csharp
public class DocSaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elDoc formato. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(SaveFormat) | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elDoc or Dot formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permiten incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento que se guarda. El valor predeterminado es **falso** . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | cuando`falso` , los metarchivos pequeños no se comprimen por motivos de rendimiento. El valor predeterminado es **verdadero** , todos los metarchivos se comprimen independientemente de su tamaño. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **cuerda vacía** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando es verdadero, hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es **verdadero** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Obtiene/establece una contraseña para cifrar el documento mediante el método de cifrado RC4. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serDoc oDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | cuando`falso` , los datos de PictureBullet no se guardan en el documento de salida. El valor predeterminado es **verdadero** . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | cuando`falso` , los datos de RoutingSlip no se guardan en el documento de salida. El valor predeterminado es **verdadero** . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |

### Observaciones

Por el momento proporciona sólo el[`SaveFormat`](./saveformat/) propiedad, pero en el futuro se agregarán otras opciones, como una contraseña de cifrado o una configuración de firma digital.

### Ejemplos

Muestra cómo configurar las opciones de guardado para formatos de Microsoft Word más antiguos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Establecer una contraseña que protegerá la carga del documento por Microsoft Word o Aspose.Words.
// Tenga en cuenta que esto no cifra el contenido del documento de ninguna manera.
options.Password = "MyPassword";

// Si el documento contiene una hoja de enrutamiento, podemos conservarlo mientras se guarda configurando este indicador en verdadero.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Para poder cargar el documento,
// necesitaremos aplicar la contraseña que especificamos en el objeto DocSaveOptions en un objeto LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [SaveOptions](../saveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
