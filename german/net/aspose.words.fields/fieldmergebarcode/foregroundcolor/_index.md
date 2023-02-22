---
title: FieldMergeBarcode.ForegroundColor
second_title: Aspose.Words für .NET-API-Referenz
description: FieldMergeBarcode eigendom. Ermittelt oder setzt die Vordergrundfarbe des BarcodeSymbols. Gültige Werte liegen im Bereich 0 0xFFFFFF
type: docs
weight: 100
url: /de/net/aspose.words.fields/fieldmergebarcode/foregroundcolor/
---
## FieldMergeBarcode.ForegroundColor property

Ermittelt oder setzt die Vordergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF]

```csharp
public string ForegroundColor { get; set; }
```

### Beispiele

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


