---
title: FieldXE.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera dina FieldXE-textegenskaper utan ansträngning. Hämta eller ställ enkelt inmatningstext för sömlös datahantering och förbättrad användarupplevelse.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Hämtar eller ställer in texten för posten.

```csharp
public string Text { get; set; }
```

## Exempel

Visar hur man skapar ett INDEX-fält och sedan använder XE-fält för att fylla det med poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som finns i dokumentet.
// Varje post visar XE-fältets egenskapsvärde för text på vänster sida
// och sidan som innehåller XE-fältet till höger.
// Om XE-fälten har samma värde i sin "Text"-egenskap,
// INDEX-fältet grupperar dem i en post.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurera INDEX-fältet för att endast visa XE-fält som ligger inom gränserna
// av ett bokmärke med namnet "MainBookmark", och vars "EntryType"-egenskaper har värdet "A".
// För både INDEX- och XE-fälten använder egenskapen "EntryType" endast det första tecknet i sitt strängvärde.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// På en ny sida, börja bokmärket med ett namn som matchar värdet
// av INDEX-fältets egenskap "BookmarkName".
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX-fältet kommer att hämta den här posten eftersom den finns inuti bokmärket,
// och dess posttyp matchar även INDEX-fältets posttyp.
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
// eftersom det ligger utanför bokmärkets gränser.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

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

* class [FieldXE](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
