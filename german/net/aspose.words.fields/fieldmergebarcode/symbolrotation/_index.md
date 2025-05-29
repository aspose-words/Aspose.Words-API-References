---
title: FieldMergeBarcode.SymbolRotation
linktitle: SymbolRotation
articleTitle: SymbolRotation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldMergeBarcode SymbolRotation“, um die Rotation von Barcode-Symbolen einfach anzupassen. Verbessern Sie Ihre Datenpräsentation mit gültigen Werten wie 0 und 3.
type: docs
weight: 140
url: /de/net/aspose.words.fields/fieldmergebarcode/symbolrotation/
---
## FieldMergeBarcode.SymbolRotation property

Ruft die Rotation des Barcodesymbols ab oder legt sie fest. Gültige Werte sind [0, 3]

```csharp
public string SymbolRotation { get; set; }
```

## Beispiele

Zeigt, wie ein Serienbrief mit QR-Barcodes erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Serienbriefs Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte „MyQRCode“ einer zusammengeführten Datenquelle in QR-Codes.
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
// Der Serienbrief erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld.
// wodurch ein QR-Code mit dem Wert aus der zusammengeführte Zeile angezeigt wird.
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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
