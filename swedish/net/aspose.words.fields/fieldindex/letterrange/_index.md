---
title: FieldIndex.LetterRange
linktitle: LetterRange
articleTitle: LetterRange
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldIndex LetterRange för att effektivt ställa in eller hämta ett specifikt bokstavsintervall och optimera indexeringsprestanda.
type: docs
weight: 90
url: /sv/net/aspose.words.fields/fieldindex/letterrange/
---
## FieldIndex.LetterRange property

Hämtar eller ställer in ett intervall av bokstäver som begränsar indexet.

```csharp
public string LetterRange { get; set; }
```

## Exempel

Visar hur man fyller ett INDEX-fält med poster med hjälp av XE-fält, och även ändrar dess utseende.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för Text på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// Om XE-fälten har samma värde i sin "Text"-egenskap,
// INDEX-fältet grupperar dem i en post.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Om du ställer in egenskapens värde på "A" grupperas alla poster efter deras första bokstav,
// och placera den bokstaven med versal ovanför varje grupp.
index.Heading = "A";

// Ställ in tabellen som skapas av INDEX-fältet så att den sträcker sig över 2 kolumner.
index.NumberOfColumns = "2";

// Ställ in alla poster med startbokstäver utanför teckenintervallet "ac" som utelämnade.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Dessa två nästa XE-fält kommer att visas under rubriken "A",
// med deras respektive textformateringar även tillämpade på deras sidnummer.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Båda de två nästföljande XE-fälten kommer att finnas under rubrikerna "B" och "C" i innehållsförteckningen för INDEX-fälten.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX-fält sorterar alla poster alfabetiskt, så den här posten visas under "A" med de andra två.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Den här posten visas inte eftersom den börjar med bokstaven "D",
// vilket ligger utanför teckenintervallet "ac" som definieras av egenskapen LetterRange i INDEX-fältet.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Se även

* class [FieldIndex](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
