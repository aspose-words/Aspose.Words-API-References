---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words para .NET
description: Desbloquee potentes funciones de combinación de correspondencia con la clase Aspose.Words.MailMerging.MailMerge. ¡Agilice la creación de documentos y mejore su productividad sin esfuerzo!
type: docs
weight: 4530
url: /es/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Representa la funcionalidad de combinación de correspondencia.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Artículo de documentación.

```csharp
public class MailMerge
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Obtiene o establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse siRemoveEmptyParagraphs Se especifica la opción. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Se produce durante la combinación de correspondencia cuando se encuentra un campo de combinación de correspondencia en el documento. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Permite manejar eventos particulares durante la combinación de correspondencia. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Devuelve una colección que representa campos de datos asignados para la operación de combinación de correspondencia. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Obtiene o establece un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse durante la ejecución de una combinación de correspondencia con regiones contra la fuente de datos o solo la primera. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Obtiene o establece un valor que indica si los campos de todo el documento se actualizan mientras se ejecuta una combinación de correspondencia con regiones. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Obtiene o establece un valor que indica si se deben conservar las etiquetas "bigote" no utilizadas. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Obtiene o establece una etiqueta final de región de combinación de correspondencia. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Obtiene o establece una etiqueta de inicio de región de combinación de correspondencia. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Obtiene o establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Obtiene o establece un valor que indica si el[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) de la primera sección del documento y sus copias para las filas de fuentes de datos posteriores se conservan durante la combinación de correspondencia o se actualizan según el comportamiento de MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Obtiene o establece un valor que indica si los espacios iniciales y finales se eliminan de los valores de combinación de correspondencia. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Obtiene o establece un valor que indica si los campos de fusión y las regiones de fusión se fusionan independientemente de la condición del campo IF principal. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Cuando`verdadero` , especifica que además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en las etiquetas "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Obtiene o establece un valor que indica si se incluye todo el párrafo con**Inicio de tabla** o**Fin de la tabla** campo o rango particular entre**Inicio de tabla** y**Fin de la tabla** Los campos deben incluirse en la región de combinación de correspondencia. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Elimina los campos relacionados con la combinación de correspondencia del documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Realiza la combinación de correspondencia desde un**Fila de datos** en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Realiza la fusión de correspondencia desde un DataTable al documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Realiza la combinación de correspondencia desde un**Vista de datos** en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Realiza la combinación de correspondencia desde**Lector de datos IDataReader** en el documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Realiza una combinación de correspondencia desde una fuente de datos personalizada. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Realiza la fusión de correspondencia desde un objeto Recordset ADO en el documento. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Realiza la combinación de correspondencia desde un**Conjunto de datos** en un documento con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Realiza la combinación de correspondencia desde un**Tabla de datos** en el documento con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Realiza la combinación de correspondencia desde un**Vista de datos** en el documento con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Realiza una combinación de correspondencia desde una fuente de datos personalizada con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Realiza una combinación de correspondencia desde una fuente de datos personalizada con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Realiza la combinación de correspondencia desde**Lector de datos IDataReader** en el documento con regiones de combinación de correspondencia. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Realiza la combinación de correspondencia desde un objeto Recordset ADO en el documento con regiones de combinación de correspondencia. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en el documento. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Devuelve una colección de regiones de combinación de correspondencia con el nombre especificado. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Devuelve una jerarquía completa de regiones (con campos) disponibles en el documento. |

## Observaciones

Para que la combinación de correspondencia funcione, el documento debe contener los campos MERGEFIELD y de Word, y opcionalmente, NEXT. Durante la combinación de correspondencia, los campos del documento se reemplazan con valores de la fuente de datos.

Hay dos formas distintas de utilizar la combinación de correspondencia: con regiones de combinación de correspondencia y sin ellas.

La combinación de correspondencia más sencilla es sin regiones y es muy similar a cómo funciona mail merge en Word. UsarEjecutar métodos para fusionar información de alguna fuente de datos como**Tabla de datos** ,**Conjunto de datos** ,**Vista de datos** ,**Lector de datos IDataReader** o una matriz de objetos en su documento. El `MailMerge` El objeto procesa todos los registros de la fuente de datos y copia y agrega contenido de todo el documento para cada registro.

Tenga en cuenta que cuando`MailMerge`El objeto encuentra un campo NEXT, selecciona el siguiente registro en la fuente de datos y continúa fusionando sin copiar ningún contenido.

Usar[`ExecuteWithRegions`](./executewithregions/) y otras sobrecargas para fusionar información en un documento con regiones de combinación de correspondencia definidas. Puede usar **Conjunto de datos** ,**Tabla de datos** ,**Vista de datos** o**Lector de datos IDataReader** como fuentes de datos para esta operación.

Necesita usar regiones de combinación de correspondencia si desea ampliar dinámicamente partes dentro del documento . Sin ellas, todo el documento se repetirá para cada registro de la fuente de datos .

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    A continuación se muestran dos formas de utilizar una DataTable como fuente de datos para una combinación de correspondencia.
    // 1 - Utilice la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento fuente de combinación de correspondencia.
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
