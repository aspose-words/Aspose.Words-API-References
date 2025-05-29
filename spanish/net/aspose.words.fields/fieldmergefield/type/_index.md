---
title: FieldMergeField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tipo FieldMergeField para acceder sin esfuerzo a los tipos de campos de Microsoft Word y mejorar sus capacidades de automatización de documentos.
type: docs
weight: 70
url: /es/net/aspose.words.fields/fieldmergefield/type/
---
## FieldMergeField.Type property

Obtiene el tipo de campo de Microsoft Word.

```csharp
public override FieldType Type { get; }
```

## Ejemplos

Muestra cómo utilizar los campos MERGEFIELD para realizar una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree una tabla de datos que se utilizará como fuente de datos de combinación de correspondencia.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Inserte un MERGEFIELD con una propiedad FieldName establecida en el nombre de una columna en la fuente de datos.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

//Podemos aplicar texto antes y después del valor que acepta este campo cuando se realiza la fusión.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Inserte otro MERGEFIELD para una columna diferente en la fuente de datos.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Ver también

* enum [FieldType](../../fieldtype/)
* class [FieldMergeField](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
