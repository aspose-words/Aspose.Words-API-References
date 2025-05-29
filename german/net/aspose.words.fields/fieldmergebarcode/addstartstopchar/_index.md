---
title: FieldMergeBarcode.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: Aspose.Words für .NET
description: Steuern Sie Start-/Stoppzeichen für NW7- und CODE39-Barcodes mit der FieldMergeBarcode-Eigenschaft AddStartStopChar. Erweitern Sie noch heute Ihre Barcode-Funktionalität!
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

Ruft ab oder legt fest, ob Start-/Stoppzeichen für die Barcodetypen NW7 und CODE39 hinzugefügt werden sollen.

```csharp
public bool AddStartStopChar { get; set; }
```

## Beispiele

Zeigt, wie ein Serienbrief mit CODE39-Barcodes erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein MERGEBARCODE-Feld ein, das während eines Serienbriefs Werte aus einer Datenquelle akzeptiert.
// Dieses Feld konvertiert alle Werte in der Spalte „MyCODE39Barcode“ einer zusammengeführten Datenquelle in CODE39-Barcodes.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Bearbeiten Sie das Erscheinungsbild, um Start-/Stoppzeichen anzuzeigen.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Erstellen Sie eine DataTable mit einer Spalte mit demselben Namen wie der BarcodeValue unseres MERGEBARCODE-Felds.
// Der Serienbrief erstellt für jede Zeile eine neue Seite. Jede Seite enthält ein DISPLAYBARCODE-Feld.
// wodurch ein CODE39-Barcode mit dem Wert aus der zusammengeführte Zeile angezeigt wird.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

### Siehe auch

* class [FieldMergeBarcode](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
