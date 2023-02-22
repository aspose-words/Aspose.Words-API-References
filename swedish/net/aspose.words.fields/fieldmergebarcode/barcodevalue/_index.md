---
title: FieldMergeBarcode.BarcodeValue
second_title: Aspose.Words för .NET API Referens
description: FieldMergeBarcode fast egendom. Hämtar eller ställer in streckkodsvärdet.
type: docs
weight: 50
url: /sv/net/aspose.words.fields/fieldmergebarcode/barcodevalue/
---
## FieldMergeBarcode.BarcodeValue property

Hämtar eller ställer in streckkodsvärdet.

```csharp
public string BarcodeValue { get; set; }
```

### Exempel

Visar hur man utför en brevkoppling på EAN13 streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett MERGEBARCODE-fält, som kommer att acceptera värden från en datakälla under en e-postkoppling.
// Detta fält kommer att konvertera alla värden i en sammanslagningsdatakällas kolumn "MyEAN13Barcode" till EAN13 streckkoder.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Visa streckkodens numeriska värde under staplarna.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Skapa en DataTable med en kolumn med samma namn som vårt MERGEBARCODE-fälts BarcodeValue.
// Brevkopplingen skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// som kommer att visa en EAN13 streckkod med värdet från den sammanslagna raden.
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

Visar hur man utför en sammanfogning på QR-streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett MERGEBARCODE-fält, som kommer att acceptera värden från en datakälla under en e-postkoppling.
// Detta fält kommer att konvertera alla värden i en sammanslagningsdatakällas "MyQRCode"-kolumn till QR-koder.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Använd anpassade färger och skalning.
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

// Skapa en DataTable med en kolumn med samma namn som vårt MERGEBARCODE-fälts BarcodeValue.
// Brevkopplingen skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// som kommer att visa en QR-kod med värdet från den sammanslagna raden.
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

### Se även

* class [FieldMergeBarcode](../)
* namnutrymme [Aspose.Words.Fields](../../fieldmergebarcode/)
* hopsättning [Aspose.Words](../../../)


