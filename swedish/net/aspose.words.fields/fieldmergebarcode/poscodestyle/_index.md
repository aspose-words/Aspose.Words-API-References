---
title: FieldMergeBarcode.PosCodeStyle
second_title: Aspose.Words för .NET API Referens
description: FieldMergeBarcode fast egendom. Hämtar eller ställer in stilen för en streckkod för försäljningsställen streckkodstyperna UPCAUPCEEAN13EAN8. De giltiga värdena okänsliga skiftlägen är STDSUP2SUP5CASE.
type: docs
weight: 110
url: /sv/net/aspose.words.fields/fieldmergebarcode/poscodestyle/
---
## FieldMergeBarcode.PosCodeStyle property

Hämtar eller ställer in stilen för en streckkod för försäljningsställen (streckkodstyperna UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). De giltiga värdena (okänsliga skiftlägen) är [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

### Exempel

Visar hur man utför en brevkoppling på EAN13 streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett MERGEBARCODE-fält, som kommer att acceptera värden från en datakälla under en e-postkoppling.
// Det här fältet konverterar alla värden i en sammanslagningsdatakällas kolumn "MyEAN13Barcode" till EAN13-streckkoder.
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

### Se även

* class [FieldMergeBarcode](../)
* namnutrymme [Aspose.Words.Fields](../../fieldmergebarcode/)
* hopsättning [Aspose.Words](../../../)


