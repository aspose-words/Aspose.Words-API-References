---
title: FieldXE
second_title: Aspose.Words för .NET API Referens
description: Implementerar XE-fältet.
type: docs
weight: 2450
url: /sv/net/aspose.words.fields/fieldxe/
---
## FieldXE class

Implementerar XE-fältet.

```csharp
public class FieldXE : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldXE](fieldxe)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end) { get; } | Hämtar noden som representerar fältänden. |
| [EntryType](../../aspose.words.fields/fieldxe/entrytype) { get; set; } | Hämtar eller ställer in en indexposttyp. |
| [Format](../../aspose.words.fields/field/format) { get; } | Får en[`FieldFormat`](../fieldformat) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsBold](../../aspose.words.fields/fieldxe/isbold) { get; set; } | Hämtar eller ställer in om fet formatering ska tillämpas på postens sidnummer. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsItalic](../../aspose.words.fields/fieldxe/isitalic) { get; set; } | Hämtar eller ställer in om kursiv formatering ska tillämpas på postens sidnummer. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [PageNumberReplacement](../../aspose.words.fields/fieldxe/pagenumberreplacement) { get; set; } | Hämtar eller ställer in text som används i stället för ett sidnummer. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldxe/pagerangebookmarkname) { get; set; } | Hämtar eller ställer in namnet på bokmärket som markerar ett intervall av sidor som infogas som postens sidnummer. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Hämtar noden som representerar början av fältet. |
| [Text](../../aspose.words.fields/fieldxe/text) { get; set; } | Hämtar eller ställer in texten i posten. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Hämtar fälttypen Microsoft Word. |
| [Yomi](../../aspose.words.fields/fieldxe/yomi) { get; set; } | Hämtar eller ställer in yomi (första fonetiska tecknet för att sortera index) för indexentry |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Definierar texten och sidnumret för en indexpost, som används av ett INDEX-fält.

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

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Se även

* class [Field](../field)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
