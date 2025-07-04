---
title: FieldMergeBarcode.FixCheckDigit
linktitle: FixCheckDigit
articleTitle: FixCheckDigit
second_title: Aspose.Words for .NET
description: Optimize your FieldMergeBarcode with the FixCheckDigit property to ensure accurate check digit validation and enhance data integrity effortlessly.
type: docs
weight: 90
url: /net/aspose.words.fields/fieldmergebarcode/fixcheckdigit/
---
## FieldMergeBarcode.FixCheckDigit property

Gets or sets whether to fix the check digit if it’s invalid.

```csharp
public bool FixCheckDigit { get; set; }
```

## Examples

Shows how to perform a mail merge on EAN13 barcodes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
// This field will convert all values in a merge data source's "MyEAN13Barcode" column into EAN13 barcodes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Display the numeric value of the barcode underneath the bars.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.That(field.Type, Is.EqualTo(FieldType.FieldMergeBarcode));
Assert.That(field.GetFieldCode(), Is.EqualTo(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x"));
builder.Writeln();

// Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
// The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
// which will display an EAN13 barcode with the value from the merged row.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields[0].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[0].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x"));
Assert.That(doc.Range.Fields[1].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[1].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x"));

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

### See Also

* class [FieldMergeBarcode](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
