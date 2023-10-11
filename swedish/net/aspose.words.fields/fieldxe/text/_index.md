---
title: FieldXE.Text
second_title: Aspose.Words för .NET API Referens
description: FieldXE fast egendom. Hämtar eller ställer in texten i posten.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Hämtar eller ställer in texten i posten.

```csharp
public string Text { get; set; }
```

### Exempel

Visar hur man skapar ett INDEX-fält och sedan använder XE-fält för att fylla i det med poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida
// och sidan som innehåller XE-fältet till höger.
// Om XE-fälten har samma värde i egenskapen "Text",
// INDEX-fältet grupperar dem i en post.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurera INDEX-fältet för att endast visa XE-fält som ligger inom gränserna
// av ett bokmärke som heter "MainBookmark", och vars "EntryType"-egenskaper har värdet "A".
// För både INDEX- och XE-fält använder egenskapen "EntryType" endast det första tecknet i dess strängvärde.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// På en ny sida börjar du bokmärket med ett namn som matchar värdet
// av INDEX-fältets "BookmarkName"-egenskap.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX-fältet kommer att plocka upp denna post eftersom den är inuti bokmärket,
// och dess inmatningstyp matchar också INDEX-fältets inmatningstyp.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Infoga ett XE-fält som inte kommer att visas i INDEX eftersom posttyperna inte matchar.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Avsluta bokmärket och infoga ett XE-fält efteråt.
// Det är av samma typ som INDEX-fältet, men kommer inte att visas
// eftersom det är utanför bokmärkets gränser.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

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
* namnutrymme [Aspose.Words.Fields](../../fieldxe/)
* hopsättning [Aspose.Words](../../../)


