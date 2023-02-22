---
title: FieldMergeBarcode.BarcodeValue
second_title: Aspose.Words für .NET-API-Referenz
description: FieldMergeBarcode eigendom. Ruft den Barcodewert ab oder legt ihn fest.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldmergebarcode/barcodevalue/
---
## FieldMergeBarcode.BarcodeValue property

Ruft den Barcodewert ab oder legt ihn fest.

```csharp
public string BarcodeValue { get; set; }
```

### Beispiele

Zeigt, wie Sie einen Seriendruck für EAN13-Barcodes durchführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Seriendrucks Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte "MyEAN13Barcode" einer Zusammenführungsdatenquelle in EAN13-Barcodes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Zeigt den numerischen Wert des Barcodes unter den Balken an.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Erstellen Sie eine DataTable mit einer Spalte mit demselben Namen wie der BarcodeValue unseres MERGEBARCODE-Felds.
// Der Seriendruck erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld,
// wodurch ein EAN13-Barcode mit dem Wert aus der zusammengeführten Zeile angezeigt wird.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

Zeigt, wie Sie einen Seriendruck für QR-Barcodes durchführen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Seriendrucks Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte „MyQRCode“ einer Zusammenführungsdatenquelle in QR-Codes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Benutzerdefinierte Farben und Skalierung anwenden.
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

// Erstellen Sie eine DataTable mit einer Spalte mit demselben Namen wie der BarcodeValue unseres MERGEBARCODE-Felds.
// Der Seriendruck erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld,
// wodurch ein QR-Code mit dem Wert aus der zusammengeführten Zeile angezeigt wird.
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

### Siehe auch

* class [FieldMergeBarcode](../)
* namensraum [Aspose.Words.Fields](../../fieldmergebarcode/)
* Montage [Aspose.Words](../../../)


