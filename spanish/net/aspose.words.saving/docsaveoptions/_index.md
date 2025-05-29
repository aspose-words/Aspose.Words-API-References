---
title: DocSaveOptions Class
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: Aspose.Words para .NET
description: Optimice el guardado de documentos con Aspose.Words.Saving.DocSaveOptions. Personalice sus formatos Doc y Dot para obtener mayor calidad y flexibilidad.
type: docs
weight: 5680
url: /es/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elDoc o Dot formato.

Para obtener más información, visite el[Especificar opciones de guardado](https://docs.aspose.com/words/net/specify-save-options/) Artículo de documentación.

```csharp
public class DocSaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elDoc formato. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elDoc o Dot formato. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe permitir la incrustación de fuentes con contornos PostScript al incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado es`FALSO` . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | Cuando`FALSO` Los metarchivos pequeños no se comprimen por razones de rendimiento. El valor predeterminado es`verdadero` , todos los metarchivos se comprimen independientemente de su tamaño. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha y hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cadena vacía** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/docsaveoptions/digitalsignaturedetails/) { get; set; } | Obtiene o establece[`DigitalSignatureDetails`](../digitalsignaturedetails/) objeto utilizado para firmar un documento. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece un valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Obtiene/establece una contraseña para cifrar el documento utilizando el método de cifrado RC4. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Cuando`verdadero` , formatos bonitos de salida donde corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama al guardar un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serDoc oDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | Cuando`FALSO` , Los datos de PictureBullet no se guardan en el documento de salida. El valor predeterminado es`verdadero` . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | Cuando`FALSO` , Los datos de RoutingSlip no se guardan en el documento de salida. El valor predeterminado es`verdadero` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina si los atributos de fuente se cambiarán según el código de carácter que se esté utilizando. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) La propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) La propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se debe utilizar o no suavizado para la representación. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se deben utilizar o no algoritmos de renderizado de alta calidad (es decir, lentos). |

## Observaciones

Por el momento solo proporciona el[`SaveFormat`](./saveformat/) propiedad, pero en el futuro se agregarán otras opciones, como una contraseña de cifrado o configuraciones de firma digital.

## Ejemplos

Muestra cómo configurar las opciones de guardado para formatos más antiguos de Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Establezca una contraseña que protegerá la carga del documento por Microsoft Word o Aspose.Words.
// Tenga en cuenta que esto no encripta el contenido del documento de ninguna manera.
options.Password = "MyPassword";

// Si el documento contiene un comprobante de ruta, podemos conservarlo mientras lo guardamos estableciendo este indicador en verdadero.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

//Para poder cargar el documento,
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
