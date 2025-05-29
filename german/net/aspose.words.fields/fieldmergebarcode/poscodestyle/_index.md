---
title: FieldMergeBarcode.PosCodeStyle
linktitle: PosCodeStyle
articleTitle: PosCodeStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldMergeBarcode PosCodeStyle-Eigenschaft für anpassbare Point-of-Sale-Barcodes. Unterstützung für UPCA, EAN13 und mehr mit flexiblen Gestaltungsoptionen!
type: docs
weight: 110
url: /de/net/aspose.words.fields/fieldmergebarcode/poscodestyle/
---
## FieldMergeBarcode.PosCodeStyle property

Ruft den Stil eines Point-of-Sale-Barcodes ab oder legt ihn fest (Barcodetypen UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Die gültigen Werte (ohne Berücksichtigung der Groß-/Kleinschreibung) sind [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

## Beispiele

Zeigt, wie ein Serienbrief mit EAN13-Barcodes erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Serienbriefs Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte „MyEAN13Barcode“ einer zusammengeführten Datenquelle in EAN13-Barcodes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Den numerischen Wert des Barcodes unter den Balken anzeigen.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Erstellen Sie eine DataTable mit einer Spalte mit demselben Namen wie der BarcodeValue unseres MERGEBARCODE-Felds.
// Der Serienbrief erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld.
// wodurch ein EAN13-Barcode mit dem Wert aus der zusammengeführte Zeile angezeigt wird.
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

### Siehe auch

* class [FieldMergeBarcode](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
