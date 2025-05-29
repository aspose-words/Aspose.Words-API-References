---
title: FieldMergeBarcode.BarcodeType
linktitle: BarcodeType
articleTitle: BarcodeType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldMergeBarcode BarcodeType för att enkelt hantera och anpassa olika streckkodstyper som QR för förbättrad dataintegration.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldmergebarcode/barcodetype/
---
## FieldMergeBarcode.BarcodeType property

Hämtar eller ställer in streckkodstypen (QR, etc.)

```csharp
public string BarcodeType { get; set; }
```

## Exempel

Visar hur man utför en dokumentkoppling på ITF14-streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett fält för MERGEBARCODE, som accepterar värden från en datakälla under en dokumentkoppling.
// Det här fältet konverterar alla värden i kolumnen "MyITF14Barcode" i en sammanfogad datakälla till ITF14-streckkoder.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// Skapa en datatabell med en kolumn med samma namn som vårt MERGEBARCODE-fälts streckkodsvärde.
// Kopplad utskrifter skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// vilket visar en ITF14-streckkod med värdet från den sammanslagna raden.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

Visar hur man utför en dokumentkoppling på CODE39-streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett fält för MERGEBARCODE, som accepterar värden från en datakälla under en dokumentkoppling.
// Det här fältet konverterar alla värden i en sammanslagningsdatakällas kolumn "MyCODE39Barcode" till CODE39-streckkoder.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Redigera dess utseende för att visa start-/stopptecken.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Skapa en datatabell med en kolumn med samma namn som vårt MERGEBARCODE-fälts streckkodsvärde.
// Kopplad utskrifter skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// vilket visar en CODE39-streckkod med värdet från den sammanslagna raden.
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

Visar hur man utför en dokumentkoppling på EAN13-streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett fält för MERGEBARCODE, som accepterar värden från en datakälla under en dokumentkoppling.
// Det här fältet konverterar alla värden i kolumnen "MyEAN13Barcode" i en sammanfogad datakälla till EAN13-streckkoder.
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

// Skapa en datatabell med en kolumn med samma namn som vårt MERGEBARCODE-fälts streckkodsvärde.
// Kopplad utskrifter skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// vilket visar en EAN13-streckkod med värdet från den sammanslagna raden.
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

Visar hur man utför en dokumentkoppling på QR-streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett fält för MERGEBARCODE, som accepterar värden från en datakälla under en dokumentkoppling.
// Det här fältet konverterar alla värden i kolumnen "MyQRCode" i en sammanfogad datakälla till QR-koder.
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

// Skapa en datatabell med en kolumn med samma namn som vårt MERGEBARCODE-fälts streckkodsvärde.
// Kopplad utskrifter skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// vilket visar en QR-kod med värdet från den sammanslagna raden.
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
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
