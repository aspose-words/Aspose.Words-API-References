---
title: FieldXE.IsItalic
linktitle: IsItalic
articleTitle: IsItalic
second_title: Aspose.Words för .NET
description: FieldXE IsItalic fast egendom. Hämtar eller ställer in om kursiv formatering ska tillämpas på postens sidnummer i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldxe/isitalic/
---
## FieldXE.IsItalic property

Hämtar eller ställer in om kursiv formatering ska tillämpas på postens sidnummer.

```csharp
public bool IsItalic { get; set; }
```

## Exempel

Visar hur man fyller i ett INDEX-fält med poster med XE-fält, och även ändrar dess utseende.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post kommer att visa XE-fältets textegenskapsvärde på vänster sida,
// och numret på sidan som innehåller XE-fältet till höger.
// Om XE-fälten har samma värde i egenskapen "Text",
// INDEX-fältet grupperar dem i en post.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Om du ställer in den här egenskapens värde till "A" grupperas alla poster efter deras första bokstav,
// och placera den bokstaven med versaler ovanför varje grupp.
index.Heading = "A";

// Ställ in tabellen som skapas av INDEX-fältet så att den sträcker sig över 2 kolumner.
index.NumberOfColumns = "2";

// Ställ in att alla poster med startbokstäver utanför teckenintervallet "ac" ska utelämnas.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Dessa nästa två XE-fält kommer att dyka upp under rubriken "A",
// med deras respektive textstilar tillämpas också på deras sidnummer.
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

// Båda de två nästa XE-fälten kommer att finnas under rubrikerna "B" och "C" i INDEX-fältens innehållsförteckning.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX-fält sorterar alla poster i alfabetisk ordning, så denna post kommer att dyka upp under "A" med de andra två.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Den här posten kommer inte att visas eftersom den börjar med bokstaven "D",
// som ligger utanför teckenintervallet "ac" som INDEX-fältets LetterRange-egenskap definierar.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Se även

* class [FieldXE](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
