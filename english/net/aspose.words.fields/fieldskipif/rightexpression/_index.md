---
title: FieldSkipIf.RightExpression
linktitle: RightExpression
second_title: Aspose.Words for .NET API Reference
description: FieldSkipIf RightExpression property. Gets or sets the right part of the comparison expression in C#.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldskipif/rightexpression/
---
## RightExpression property

Gets or sets the right part of the comparison expression.

```csharp
public string RightExpression { get; set; }
```

## Examples

Shows how to skip pages in a mail merge using the SKIPIF field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a SKIPIF field. If the current row of a mail merge operation fulfills the condition
// which the expressions of this field state, then the mail merge operation aborts the current row,
// discards the current merge document, and then immediately moves to the next row to begin the next merge document.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Move the builder to the SKIPIF field's separator so we can place a MERGEFIELD inside the SKIPIF field.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// The MERGEFIELD refers to the "Department" column in our data table. If a row from that table
// has a value of "HR" in its "Department" column, then this row will fulfill the condition.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Add content to our document, create the data source, and execute the mail merge.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

// This table has three rows, and one of them fulfills the condition of our SKIPIF field. 
// The mail merge will produce two pages.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Shows how to use MERGEREC and MERGESEQ fields to the number and count mail merge records in a mail merge's output documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// A MERGEREC field will print the row number of the data being merged in every merge output document.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// A MERGESEQ field will count the number of successful merges and print the current value on each respective page.
// If a mail merge skips no rows and invokes no SKIP/SKIPIF/NEXT/NEXTIF fields, then all merges are successful.
// The MERGESEQ and MERGEREC fields will display the same results of their mail merge was successful.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Insert a SKIPIF field, which will skip a merge if the name is "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Create a data source with 3 rows, one of them having "John Doe" as a value for the "Name" column.
// Since a SKIPIF field will be triggered once by that value, the output of our mail merge will have 2 pages instead of 3.
// On page 1, the MERGESEQ and MERGEREC fields will both display "1".
// On page 2, the MERGEREC field will display "3" and the MERGESEQ field will display "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);            
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### See Also

* class [FieldSkipIf](../)
* namespace [Aspose.Words.Fields](../../fieldskipif/)
* assembly [Aspose.Words](../../../)
