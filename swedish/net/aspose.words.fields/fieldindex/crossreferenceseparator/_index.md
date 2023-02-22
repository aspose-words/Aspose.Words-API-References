---
title: FieldIndex.CrossReferenceSeparator
second_title: Aspose.Words för .NET API Referens
description: FieldIndex fast egendom. Hämtar eller ställer in teckensekvensen som används för att separera korsreferenser och andra poster.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

Hämtar eller ställer in teckensekvensen som används för att separera korsreferenser och andra poster.

```csharp
public string CrossReferenceSeparator { get; set; }
```

### Exempel

Visar hur man definierar korsreferenser i ett INDEX-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post kommer att visa XE-fältets textegenskapsvärde på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// INDEX-posten samlar alla XE-fält med matchande värden i egenskapen "Text"
// i en post i motsats till att göra en post för varje XE-fält.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Vi kan konfigurera ett XE-fält för att få dess INDEX-post att visa en sträng istället för ett sidnummer.
// Först, för poster som ersätter ett sidnummer med en sträng,
// ange en anpassad avgränsare mellan XE-fältets textegenskapsvärde och strängen.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Infoga ett XE-fält, vilket skapar en vanlig INDEX-post som visar detta fälts sidnummer,
// och anropar inte värdet CrossReferenceSeparator.
// Posten för detta XE-fält kommer att visa "Apple, 2".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Infoga ett annat XE-fält på sidan 3 och ange ett värde för egenskapen PageNumberReplacement.
// Detta värde visas istället för numret på sidan som detta fält är på,
// och INDEX-fältets CrossReferenceSeparator-värde visas framför det.
// Posten för detta XE-fält kommer att visa "Banan, se: Tropisk frukt".
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../fieldindex/)
* hopsättning [Aspose.Words](../../../)


