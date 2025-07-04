---
title: FieldMergeField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the FieldMergeField Type property to effortlessly access Microsoft Word field types and enhance your document automation capabilities.
type: docs
weight: 70
url: /net/aspose.words.fields/fieldmergefield/type/
---
## FieldMergeField.Type property

Gets the Microsoft Word field type.

```csharp
public override FieldType Type { get; }
```

## Examples

Shows how to use MERGEFIELD fields to perform a mail merge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a data table to be used as a mail merge data source.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Insert a MERGEFIELD with a FieldName property set to the name of a column in the data source.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// We can apply text before and after the value that this field accepts when the merge takes place.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.That(fieldMergeField.GetFieldCode(), Is.EqualTo(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \""));
Assert.That(fieldMergeField.Type, Is.EqualTo(FieldType.FieldMergeField));

// Insert another MERGEFIELD for a different column in the data source.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.That(doc.GetText().Trim(), Is.EqualTo("Dear Mr. Doe:\u000cDear Mrs. Cardholder:"));
```

### See Also

* enum [FieldType](../../fieldtype/)
* class [FieldMergeField](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
