---
title: TextAfter
second_title: Aspose.Words for .NET API Reference
description: FieldMergeField property. Gets or sets the text to be inserted after the field if the field is not blank in C#.
type: docs
weight: 50
url: /net/aspose.words.fields/fieldmergefield/textafter/
---
## FieldMergeField.TextAfter property

Gets or sets the text to be inserted after the field if the field is not blank.

```csharp
public string TextAfter { get; set; }
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

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Insert another MERGEFIELD for a different column in the data source.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### See Also

* class [FieldMergeField](../)
* namespace [Aspose.Words.Fields](../../fieldmergefield/)
* assembly [Aspose.Words](../../../)
