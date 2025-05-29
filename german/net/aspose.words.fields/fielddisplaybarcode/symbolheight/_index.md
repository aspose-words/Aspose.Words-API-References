---
title: FieldDisplayBarcode.SymbolHeight
linktitle: SymbolHeight
articleTitle: SymbolHeight
second_title: Aspose.Words für .NET
description: Passen Sie die SymbolHeight-Eigenschaft von FieldDisplayBarcode an, um die Barcode-Höhe in TWIPS anzupassen. Verbessern Sie Ihre Barcode-Anzeige präzise!
type: docs
weight: 130
url: /de/net/aspose.words.fields/fielddisplaybarcode/symbolheight/
---
## FieldDisplayBarcode.SymbolHeight property

Ruft die Höhe des Symbols ab oder legt sie fest. Die Einheit ist TWIPS (1/1440 Zoll).

```csharp
public string SymbolHeight { get; set; }
```

## Beispiele

Zeigt, wie ein DISPLAYBARCODE-Feld eingefügt und seine Eigenschaften festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Unten sind vier Arten von Barcodes aufgeführt, die auf verschiedene Weise gestaltet sind und die das Feld DISPLAYBARCODE anzeigen kann.
// 1 - QR-Code mit benutzerdefinierten Farben:
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

// 2 - EAN13-Barcode, mit den unter den Balken angezeigten Ziffern:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39-Barcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4-Barcode mit einem angegebenen Fallcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Siehe auch

* class [FieldDisplayBarcode](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
