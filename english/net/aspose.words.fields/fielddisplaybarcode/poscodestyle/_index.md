---
title: FieldDisplayBarcode.PosCodeStyle
linktitle: PosCodeStyle
articleTitle: PosCodeStyle
second_title: Aspose.Words for .NET
description: Discover the FieldDisplayBarcode PosCodeStyle property for customizing Point of Sale barcodes. Supports UPCA, EAN13, and more for optimal efficiency.
type: docs
weight: 110
url: /net/aspose.words.fields/fielddisplaybarcode/poscodestyle/
---
## FieldDisplayBarcode.PosCodeStyle property

Gets or sets the style of a Point of Sale barcode (barcode types UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). The valid values (case insensitive) are [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

## Examples

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

Assert.That(field.GetFieldCode(), Is.EqualTo(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0"));
builder.Writeln();

// 2 -  EAN13 barcode, with the digits displayed below the bars:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x"));
builder.Writeln();

// 3 -  CODE39 barcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.That(field.GetFieldCode(), Is.EqualTo(" DISPLAYBARCODE  12345ABCDE CODE39 \\d"));
builder.Writeln();

// 4 -  ITF4 barcode, with a specified case code:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.That(field.GetFieldCode(), Is.EqualTo(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD"));

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### See Also

* class [FieldDisplayBarcode](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
