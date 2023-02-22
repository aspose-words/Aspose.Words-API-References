---
title: MailMerge.CleanupOptions
second_title: Referencia de API de Aspose.Words para .NET
description: MailMerge propiedad. Obtiene o establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia.
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Obtiene o establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

### Ejemplos

Muestra cómo eliminar los párrafos vacíos que una combinación de correspondencia puede crear a partir del documento de salida combinado.

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

// Cree un documento con MERGEFIELDs para tres columnas de una tabla de fuente de datos de combinación de correspondencia,
// y luego crea una tabla con solo dos columnas cuyos nombres coincidan con nuestros MERGEFIELD.
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

// Nuestro tercer MERGEFIELD hace referencia a una columna "Ciudad", que no existe en nuestra fuente de datos.
// La combinación de correspondencia dejará campos como este intactos en su estado anterior a la combinación.
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

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)


