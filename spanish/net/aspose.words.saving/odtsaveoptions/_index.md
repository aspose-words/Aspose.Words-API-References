---
title: OdtSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Se puede utilizar para especificar opciones adicionales al guardar un documento en elOdt or Ott formato.
type: docs
weight: 5050
url: /es/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Se puede utilizar para especificar opciones adicionales al guardar un documento en elOdt or Ott formato.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions#constructor)() | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt formato. |
| [OdtSaveOptions](odtsaveoptions#constructor_1)(SaveFormat) | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt or Ott formato. |
| [OdtSaveOptions](odtsaveoptions#constructor_2)(string) | Inicializa una nueva instancia de esta clase que se puede usar para guardar un documento en elOdt format encriptado con una contraseña. |

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
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11) { get; set; } | Especifica si la exportación debe corresponder estrictamente a la especificación 1.1 de ODT. OOo 3.0 muestra los archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Use "falso" para este propósito, o "verdadero" para conformidad estricta con la especificación 1.1. El valor predeterminado es **falso** . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit) { get; set; } | Permite especificar unidades de medida para aplicar al contenido del documento. El valor predeterminado esCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Obtiene o establece el valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es **falso** . |
| [Password](../../aspose.words.saving/odtsaveoptions/password) { get; set; } | Obtiene o establece una contraseña para cifrar el documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | cuando`verdadero` , bonitos formatos de salida cuando corresponda. El valor predeterminado es **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Llamado durante el guardado de un documento y acepta datos sobre el progreso del guardado. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat) { get; set; } | Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serOdt oOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De manera predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Obtiene o establece un valor que determina si el[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la propiedad se actualiza antes de guardar. El valor predeterminado es falso; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Obtiene o establece un valor que determina si los campos de ciertos tipos deben actualizarse antes de guardar el documento en un formato de página fijo. El valor predeterminado para esta propiedad es **verdadero** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Obtiene o establece un valor que determina si el[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la propiedad se actualiza antes de guardar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Obtiene o establece un valor que determina si el[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la propiedad se actualiza antes de guardar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Obtiene o establece el valor que determina si el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) se actualiza antes de guardar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Obtiene o establece un valor que determina si se usa o no suavizado para renderizar. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lento). |

### Observaciones

Por el momento proporciona sólo el[`SaveFormat`](./saveformat) propiedad, pero en el futuro se agregarán otras opciones, como una contraseña de cifrado o una configuración de firma digital.

### Ejemplos

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

Muestra cómo utilizar diferentes unidades de medida para definir los parámetros de estilo de un documento ODT guardado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando exportamos el documento a .odt, podemos usar un objeto OdtSaveOptions para modificar cómo guardamos el documento.
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Centimeters"
// para definir contenido como parámetros de estilo usando el sistema métrico, que usa Open Office. 
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Inches"
// para definir contenido como parámetros de estilo usando el sistema imperial, que usa Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ver también

* class [SaveOptions](../saveoptions)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
