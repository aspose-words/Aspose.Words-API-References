---
title: OdtSaveOptions Class
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.OdtSaveOptions clase. Se puede utilizar para especificar opciones adicionales al guardar un documento en elOdt o Ott formato en C#.
type: docs
weight: 5330
url: /es/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elOdt o Ott formato.

Para obtener más información, visite el[Especificar opciones de guardar](https://docs.aspose.com/words/net/specify-save-options/) artículo de documentación.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elOdt formato. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elOdt o Ott formato. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(*string*) | Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elOdt format cifrado con una contraseña. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtiene o establece un valor booleano que indica si se permite incrustar fuentes con contornos PostScript al incrustar fuentes TrueType en un documento una vez guardado. El valor predeterminado es`FALSO` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtiene o establece la zona horaria local personalizada utilizada para los campos de fecha/hora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre del archivo). El valor predeterminado para esta propiedad es**cuerda vacía** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan las formas de DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | cuando`verdadero` , hace que el nombre y la versión de Aspose.Words se incrusten en los archivos producidos. El valor predeterminado es`verdadero` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtiene o establece un valor que determina cómo se representan los objetos de tinta (InkML). |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Especifica si la exportación debe corresponder estrictamente a la especificación ODT 1.1. OOo 3.0 muestra archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Utilice "falso" para este propósito, o "verdadero" para conformidad estricta con la especificación 1.1. El valor predeterminado es`FALSO` . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Permite especificar unidades de medida para aplicar al contenido del documento. El valor predeterminado esCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Obtiene o establece una contraseña para cifrar el documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | cuando`verdadero` salida con bonitos formatos cuando corresponda. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Se llama durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serOdt oOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Especifica la carpeta para archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es`verdadero` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtiene o establece un valor que determina si se utiliza o no el suavizado para la representación. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lentos). |

## Observaciones

Por el momento sólo proporciona el[`SaveFormat`](./saveformat/) propiedad, pero en el futuro se agregarán otras opciones, como una contraseña de cifrado o configuraciones de firma digital.

## Ejemplos

Muestra cómo hacer que un documento guardado se ajuste a un esquema ODT anterior.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Muestra cómo utilizar diferentes unidades de medida para definir parámetros de estilo de un documento ODT guardado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando exportamos el documento a .odt, podemos usar un objeto OdtSaveOptions para modificar cómo guardamos el documento.
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Centimeters"
 // para definir contenido como parámetros de estilo utilizando el sistema métrico, que utiliza Open Office.
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Inches"
// para definir contenido como parámetros de estilo utilizando el sistema imperial, que utiliza Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ver también

* class [SaveOptions](../saveoptions/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
