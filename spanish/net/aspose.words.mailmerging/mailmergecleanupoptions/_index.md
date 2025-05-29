---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.MailMergeCleanupOptions para gestionar eficientemente la limpieza de la combinación de correspondencia. Optimice sus documentos controlando la eliminación de elementos sin problemas.
type: docs
weight: 4540
url: /es/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Especifica las opciones que determinan qué elementos se eliminan durante la combinación de correspondencia.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Especifica un valor predeterminado. |
| RemoveEmptyParagraphs | `1` | Especifica si los párrafos que contienen campos de combinación de correspondencia sin datos deben eliminarse del documento. Cuando se establece esta opción, los párrafos que contienen campos de combinación de inicio y fin de región que de otro modo estarían vacíos también se eliminan. |
| RemoveUnusedRegions | `2` | Especifica si las regiones de combinación de correspondencia no utilizadas deben eliminarse del documento. |
| RemoveUnusedFields | `4` | Especifica si los campos de combinación no utilizados deben eliminarse del documento. |
| RemoveContainingFields | `8` | Especifica si los campos que contienen campos de combinación (por ejemplo, IF) deben eliminarse del documento si se eliminan los campos de combinación anidados. |
| RemoveStaticFields | `10` | Especifica si los campos estáticos deben eliminarse del documento. Los campos estáticos son aquellos cuyos resultados permanecen inalterados ante cualquier cambio en el documento. Los campos cuyos resultados no se almacenan en un documento y se calculan sobre la marcha (comoFieldListNum , FieldSymbol , etc.) no se consideran estáticos. |
| RemoveEmptyTableRows | `20` | Especifica si las filas vacías que contienen regiones de combinación de correspondencia deben eliminarse del documento. |
| RemoveEmptyTables | `40` | Especifica si se deben eliminar de las tablas del documento que contienen regiones de combinación de correspondencia que se eliminaron mediante RemoveUnusedRegions o elRemoveEmptyTableRows opción. |

## Ejemplos

Muestra cómo eliminar toda una tabla vacía durante la combinación de correspondencia.

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

Muestra cómo eliminar los párrafos vacíos que una combinación de correspondencia puede crear del documento de salida de la combinación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

Muestra cómo eliminar automáticamente los MERGEFIELD que no se utilizan durante la combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un documento con MERGEFIELDs para tres columnas de una tabla de origen de datos de combinación de correspondencia,
// y luego crea una tabla con solo dos columnas cuyos nombres coincidan con nuestros MERGEFIELDs.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

//Nuestro tercer MERGEFIELD hace referencia a una columna "Ciudad", que no existe en nuestra fuente de datos.
// La combinación de correspondencia dejará campos como éste intactos en su estado previo a la combinación.
// Establecer la propiedad "CleanupOptions" en "RemoveUnusedFields" eliminará cualquier MERGEFIELD
// que no se utilizan durante una combinación de correspondencia para limpiar los documentos combinados.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
