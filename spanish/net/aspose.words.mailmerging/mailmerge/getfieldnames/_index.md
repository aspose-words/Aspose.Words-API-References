---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words para .NET
description: Descubra el método GetFieldNames de MailMerge para acceder y utilizar sin esfuerzo todos los nombres de campos de combinación de correspondencia en su documento para una automatización optimizada de los documentos.
type: docs
weight: 220
url: /es/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en el documento.

```csharp
public string[] GetFieldNames()
```

## Observaciones

Devuelve los nombres completos de los campos de combinación, incluyendo el prefijo opcional. No elimina los nombres de campo duplicados.

Se crea una nueva matriz de cadenas en cada llamada.

Incluye nombres de campo "bigote" si[`UseNonMergeFields`](../usenonmergefields/) es`verdadero`.

## Ejemplos

Muestra cómo obtener los nombres de todos los campos de combinación en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// Para cada nombre MERGEFIELD en el documento, asegúrese de que la tabla de datos contenga una columna
 // con el mismo nombre y luego ejecutar la combinación de correspondencia.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
