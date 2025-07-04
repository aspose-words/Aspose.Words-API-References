---
title: FieldMergeBarcode.BarcodeType
linktitle: BarcodeType
articleTitle: BarcodeType
second_title: Aspose.Words for .NET
description: Discover the FieldMergeBarcode BarcodeType property to easily manage and customize various barcode types like QR for enhanced data integration.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldmergebarcode/barcodetype/
---
## FieldMergeBarcode.BarcodeType property

Gets or sets the barcode type (QR, etc.)

```csharp
public string BarcodeType { get; set; }
```

## Examples

Shows how to perform a mail merge on ITF14 barcodes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
// This field will convert all values in a merge data source's "MyITF14Barcode" column into ITF14 barcodes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.That(field.Type, Is.EqualTo(FieldType.FieldMergeBarcode));
Assert.That(field.GetFieldCode(), Is.EqualTo(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD"));

// Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
// The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
// which will display an ITF14 barcode with the value from the merged row.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields[0].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[0].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD"));
Assert.That(doc.Range.Fields[1].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[1].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD"));

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

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

Shows how to perform a mail merge on QR barcodes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a MERGEBARCODE field, which will accept values from a data source during a mail merge.
// This field will convert all values in a merge data source's "MyQRCode" column into QR codes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Apply custom colors and scaling.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.That(field.Type, Is.EqualTo(FieldType.FieldMergeBarcode));
Assert.That(field.GetFieldCode(), Is.EqualTo(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0"));
builder.Writeln();

// Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
// The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
// which will display a QR code with the value from the merged row.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields[0].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[0].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B"));
Assert.That(doc.Range.Fields[1].Type, Is.EqualTo(FieldType.FieldDisplayBarcode));
Assert.That(doc.Range.Fields[1].GetFieldCode(), Is.EqualTo("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B"));

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### See Also

* class [FieldMergeBarcode](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
