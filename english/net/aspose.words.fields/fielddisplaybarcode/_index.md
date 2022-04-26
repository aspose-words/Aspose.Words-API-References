---
title: FieldDisplayBarcode
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1580
url: /net/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class

Implements the DISPLAYBARCODE field.

```csharp
public class FieldDisplayBarcode : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldDisplayBarcode](fielddisplaybarcode)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AddStartStopChar](addstartstopchar) { get; set; } | Gets or sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [BackgroundColor](backgroundcolor) { get; set; } | Gets or sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] |
| [BarcodeType](barcodetype) { get; set; } | Gets or sets the barcode type (QR, etc.) |
| [BarcodeValue](barcodevalue) { get; set; } | Gets or sets the barcode value. |
| [CaseCodeStyle](casecodestyle) { get; set; } | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayText](displaytext) { get; set; } | Gets or sets whether to display barcode data (text) along with image. |
| [ErrorCorrectionLevel](errorcorrectionlevel) { get; set; } | Gets or sets an error correction level of QR Code. Valid values are [0, 3]. |
| [FixCheckDigit](fixcheckdigit) { get; set; } | Gets or sets whether to fix the check digit if it’s invalid. |
| [ForegroundColor](foregroundcolor) { get; set; } | Gets or sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] |
| [PosCodeStyle](poscodestyle) { get; set; } | Gets or sets the style of a Point of Sale barcode (barcode types UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). The valid values (case insensitive) are [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [ScalingFactor](scalingfactor) { get; set; } | Gets or sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000] |
| [SymbolHeight](symbolheight) { get; set; } | Gets or sets the height of the symbol. The units are in TWIPS (1/1440 inch). |
| [SymbolRotation](symbolrotation) { get; set; } | Gets or sets the rotation of the barcode symbol. Valid values are [0, 3] |

### Remarks

Inserts a barcode.

### Examples

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

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// Create a DataTable with a column with the same name as our MERGEBARCODE field's BarcodeValue.
// The mail merge will create a new page for each row. Each page will contain a DISPLAYBARCODE field,
// which will display a QR code with the value from the merged row.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

Shows how to insert a DISPLAYBARCODE field, and set its properties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
// 1 -  QR code with custom colors:
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 -  EAN13 barcode, with the digits displayed below the bars:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 -  CODE39 barcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 -  ITF4 barcode, with a specified case code:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### See Also

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
