---
title: FieldMergeBarcode Class
linktitle: FieldMergeBarcode
articleTitle: FieldMergeBarcode
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldMergeBarcode för att enkelt implementera MERGEBARCODE-fält för förbättrad dokumentautomation och effektivitet.
type: docs
weight: 2550
url: /sv/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

Implementerar fältet MERGEBARCODE.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldMergeBarcode : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar/) { get; set; } | Hämtar eller anger om start-/stopptecken ska läggas till för streckkodstyperna NW7 och CODE39. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor/) { get; set; } | Hämtar eller ställer in bakgrundsfärgen för streckkodssymbolen. Giltiga värden är inom intervallet [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype/) { get; set; } | Hämtar eller ställer in streckkodstypen (QR, etc.) |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue/) { get; set; } | Hämtar eller ställer in streckkodsvärdet. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle/) { get; set; } | Hämtar eller ställer in stilen för en ärendekod för streckkodstypen ITF14. Giltiga värden är [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext/) { get; set; } | Hämtar eller anger om streckkodsdata (text) ska visas tillsammans med bild. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel/) { get; set; } | Hämtar eller ställer in en felkorrigeringsnivå för QR-koden. Giltiga värden är [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit/) { get; set; } | Hämtar eller anger om kontrollsiffran ska korrigeras om den är ogiltig. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor/) { get; set; } | Hämtar eller ställer in förgrundsfärgen för streckkodssymbolen. Giltiga värden är inom intervallet [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle/) { get; set; } | Hämtar eller ställer in stilen på en försäljningsställesstreckkod (streckkodstyperna UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Giltiga värden (okänsliga för versaler) är [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor/) { get; set; } | Hämtar eller ställer in en skalningsfaktor för symbolen. Värdet anges i hela procentenheter och de giltiga värdena är [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight/) { get; set; } | Hämtar eller ställer in symbolens höjd. Enheterna är i TWIPS (1/1440 tum). |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation/) { get; set; } | Hämtar eller ställer in rotationen för streckkodssymbolen. Giltiga värden är [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Koppla ut en streckkod.

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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
