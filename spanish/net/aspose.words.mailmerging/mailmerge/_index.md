---
title: Class MailMerge
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.MailMerging.MailMerge clase. Representa la función de combinación de correspondencia.
type: docs
weight: 3620
url: /es/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Representa la función de combinación de correspondencia.

```csharp
public class MailMerge
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Obtiene o establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse si elRemoveEmptyParagraphs se especifica la opción. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Ocurre durante la combinación de correspondencia cuando se encuentra un campo de combinación de correspondencia en el documento. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Permite manejar eventos particulares durante la combinación de correspondencia. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Devuelve una colección que representa campos de datos asignados para la operación de combinación de correspondencia. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Obtiene o establece un valor que indica si todas las regiones de combinación de correo del documento con el nombre de un origen de datos se deben combinar al ejecutar una combinación de correo con regiones en el origen de datos o solo la primera. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Obtiene o establece un valor que indica si los campos de todo el documento se actualizan al ejecutar una combinación de correspondencia con regiones. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Obtiene o establece un valor que indica si se deben conservar las etiquetas "bigote" no utilizadas. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Obtiene o establece una etiqueta final de región de combinación de correspondencia. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Obtiene o establece una etiqueta de inicio de región de combinación de correspondencia. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Obtiene o establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Obtiene o establece un valor que indica si el[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) de la primera sección del documento y sus copias para las filas de fuente de datos subsiguientes se conservan durante la combinación de correspondencia o se actualizan de acuerdo con el comportamiento de MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Obtiene o establece un valor que indica si los espacios en blanco iniciales y finales se eliminan de los valores de combinación de correspondencia. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Obtiene o establece un valor que indica si los campos de fusión y las regiones de fusión se fusionan independientemente de la condición del campo IF principal. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Cuando es verdadero, especifica que además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en las etiquetas "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Obtiene o establece un valor que indica si el párrafo completo con el campo TableStart o TableEnd o un rango particular entre los campos TableStart y TableEnd debe incluirse en la región de combinación de correspondencia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Elimina los campos relacionados con la combinación de correspondencia del documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | Realiza la combinación de correspondencia de un DataRow en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | Realiza la combinación de correspondencia de un DataTable en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | Realiza la combinación de correspondencia de un DataView en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | Realiza la combinación de correspondencia de IDataReader en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | Realiza una combinación de correspondencia desde una fuente de datos personalizada. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | Realiza una operación de combinación de correspondencia para un solo registro. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | Realiza la combinación de correo desde un objeto Recordset de ADO en el documento. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | Realiza la combinación de correspondencia de un conjunto de datos en un documento con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | Realiza la combinación de correspondencia de un DataTable en el documento con las regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | Realiza la combinación de correspondencia desde un DataView en el documento con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | Realiza una combinación de correspondencia desde un origen de datos personalizado con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | Realiza una combinación de correspondencia desde un origen de datos personalizado con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | Realiza la combinación de correspondencia de IDataReader en el documento con las regiones de combinación de correspondencia. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | Realiza la combinación de correspondencia desde un objeto Recordset de ADO en el documento con regiones de combinación de correspondencia. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en el documento. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | Devuelve una colección de regiones de combinación de correspondencia con el nombre especificado. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Devuelve una jerarquía completa de regiones (con campos) disponibles en el documento. |

### Observaciones

Para que la operación de combinación de correspondencia funcione, el documento debe contener Word MERGEFIELD y opcionalmente campos NEXT. Durante la operación de combinación de correspondencia, los campos de combinación en el documento son reemplazados con valores de su fuente de datos.

Hay dos formas distintas de usar la combinación de correspondencia: con regiones de combinación de correspondencia y sin ellas.

La combinación de correspondencia más simple es sin regiones y es muy similar a cómo funciona la combinación de correspondencia en Word. UsarEjecutar métodos para fusionar información de alguna fuente de datos como **Tabla de datos** , **conjunto de datos** , **vista de datos** , **IDataReader** o una matriz de objetos en su documento. El  **Unificación de correo** El objeto procesa todos los registros de la fuente de datos y copia y agrega contenido de todo el documento para cada registro.

Tenga en cuenta que cuando **Unificación de correo**el objeto encuentra un campo SIGUIENTE, selecciona el siguiente registro en la fuente de datos y continúa fusionándose sin copiar ningún contenido.

UsarEjecutarConRegiones métodos para combinar información en un documento con regiones de combinación de correspondencia definidas. Puedes usar  **conjunto de datos** , **Tabla de datos** , **vista de datos** o **IDataReader** como fuentes de datos para esta operación.

Debe usar regiones de combinación de correspondencia si desea aumentar dinámicamente las partes dentro del documento . Sin las regiones de combinación de correspondencia, el documento completo se repetirá para cada registro de la fuente de datos.

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // A continuación se muestran dos formas de usar un DataTable como fuente de datos para una combinación de correspondencia.
    // 1: use la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento de origen de combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)


