---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldXE PageNumberReplacement för att enkelt anpassa sidnummertext för förbättrad dokumentformatering och läsbarhet.
type: docs
weight: 50
url: /sv/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Hämtar eller ställer in text som används istället för ett sidnummer.

```csharp
public string PageNumberReplacement { get; set; }
```

## Exempel

Visar hur man definierar korsreferenser i ett INDEX-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för Text på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// INDEX-posten samlar in alla XE-fält med matchande värden i egenskapen "Text"
// till en post istället för att skapa en post för varje XE-fält.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Vi kan konfigurera ett XE-fält så att dess INDEX-post visar en sträng istället för ett sidnummer.
// Först, för poster som ersätter ett sidnummer med en sträng,
// ange en anpassad avgränsare mellan XE-fältets egenskapsvärde Text och strängen.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Infoga ett XE-fält, vilket skapar en vanlig INDEX-post som visar fältets sidnummer,
// och anropar inte CrossReferenceSeparator-värdet.
// Posten för detta XE-fält kommer att visa "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Infoga ett annat XE-fält på sidan 3 och ange ett värde för egenskapen PageNumberReplacement.
// Detta värde kommer att visas istället för numret på den sida som fältet finns på,
// och INDEX-fältets CrossReferenceSeparator-värde kommer att visas framför det.
// Posten för detta XE-fält visar "Banan, se: Tropisk frukt".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Se även

* class [FieldXE](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
