---
title: FieldMergeBarcode.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: Aspose.Words for .NET
description: Control Start/Stop characters for NW7 and CODE39 barcodes with the FieldMergeBarcode AddStartStopChar property. Enhance your barcode functionality today!
type: docs
weight: 20
url: /net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

Gets or sets whether to add Start/Stop characters for barcode types NW7 and CODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

## Examples

Shows how to perform a mail merge on CODE39 barcodes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
// This field will convert all values in a merge data source's "MyCODE39Barcode" column into CODE39 barcodes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Edit its appearance to display start/stop characters.
field.AddStartStopChar = true;

Assert.That(field.Type, Is.EqualTo(FieldType.FieldMergeBarcode));
Assert.That(field.GetFieldCode(), Is.EqualTo(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d"));
builder.Writeln();

// Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
// The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
// which will display a CODE39 barcode with the value from the merged row.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields[0].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[0].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d"));
Assert.That(doc.Range.Fields[1].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[1].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d"));

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

### See Also

* class [FieldMergeBarcode](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
