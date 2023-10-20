---
title: FieldMergeBarcode.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: Aspose.Words för .NET
description: FieldMergeBarcode AddStartStopChar fast egendom. Hämtar eller ställer in om start/stopptecken ska läggas till för streckkodstyperna NW7 och CODE39 i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

Hämtar eller ställer in om start/stopp-tecken ska läggas till för streckkodstyperna NW7 och CODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

## Exempel

Visar hur man utför en brevkoppling på CODE39 streckkoder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett MERGEBARCODE-fält, som kommer att acceptera värden från en datakälla under en e-postkoppling.
// Det här fältet konverterar alla värden i en sammanslagningsdatakällas kolumn "MyCODE39Barcode" till CODE39-streckkoder.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Redigera dess utseende för att visa start/stopp-tecken.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Skapa en DataTable med en kolumn med samma namn som vårt MERGEBARCODE-fälts BarcodeValue.
// Brevkopplingen skapar en ny sida för varje rad. Varje sida kommer att innehålla ett DISPLAYBARCODE-fält,
// som kommer att visa en CODE39 streckkod med värdet från den sammanslagna raden.
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

### Se även

* class [FieldMergeBarcode](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
