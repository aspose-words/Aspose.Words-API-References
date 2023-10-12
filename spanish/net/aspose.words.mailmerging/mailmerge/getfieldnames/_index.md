---
title: MailMerge.GetFieldNames
second_title: Referencia de API de Aspose.Words para .NET
description: MailMerge método. Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en el documento.
type: docs
weight: 220
url: /es/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en el documento.

```csharp
public string[] GetFieldNames()
```

### Observaciones

Devuelve nombres completos de campos de combinación, incluido el prefijo opcional. No elimina nombres de campos duplicados.

Se crea una nueva matriz de cadenas en cada llamada.

Incluye nombres de campos "bigote" si[`UseNonMergeFields`](../usenonmergefields/) es`verdadero`.

### Ejemplos

Muestra cómo obtener nombres de todos los campos de combinación en un documento.

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
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)


