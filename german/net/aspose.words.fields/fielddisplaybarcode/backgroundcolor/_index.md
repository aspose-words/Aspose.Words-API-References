---
title: FieldDisplayBarcode.BackgroundColor
second_title: Aspose.Words für .NET-API-Referenz
description: FieldDisplayBarcode eigendom. Liest oder setzt die Hintergrundfarbe des BarcodeSymbols. Gültige Werte liegen im Bereich 0 0xFFFFFF
type: docs
weight: 30
url: /de/net/aspose.words.fields/fielddisplaybarcode/backgroundcolor/
---
## FieldDisplayBarcode.BackgroundColor property

Liest oder setzt die Hintergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF]

```csharp
public string BackgroundColor { get; set; }
```

### Beispiele

Zeigt, wie ein DISPLAYBARCODE-Feld eingefügt und seine Eigenschaften festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Unten sind vier Arten von Strichcodes, die auf verschiedene Arten dekoriert sind und die das DISPLAYBARCODE-Feld anzeigen kann.
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

// 2 - EAN13-Barcode, wobei die Ziffern unter den Balken angezeigt werden:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39-Strichcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4-Barcode mit einem bestimmten Fallcode:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Siehe auch

* class [FieldDisplayBarcode](../)
* namensraum [Aspose.Words.Fields](../../fielddisplaybarcode/)
* Montage [Aspose.Words](../../../)


