---
title: FieldIndex Class
linktitle: FieldIndex
articleTitle: FieldIndex
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldIndex för att enkelt implementera INDEX-fält i dina dokument. Förbättra din dokumenthantering idag!
type: docs
weight: 2470
url: /sv/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implementerar INDEX-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldIndex : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldIndex](fieldindex/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Hämtar eller anger namnet på bokmärket som markerar den del av dokumentet som används för att bygga indexet. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera korsreferenser och andra poster. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Hämtar eller anger en indexposttyp som används för att bygga indexet. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Hämtar ett värde som anger om en sidnummeravgränsare åsidosätts genom fältets kod. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Hämtar ett värde som anger om en sekvens ska användas medan fältets resultat skapas. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Hämtar eller anger en rubrik som visas i början av varje uppsättning poster för en given bokstav. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Hämtar eller anger språk-ID:t som används för att generera indexet. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Hämtar eller ställer in ett intervall av bokstäver som begränsar indexet. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Hämtar eller anger antalet kolumner per sida som används vid uppbyggnad av indexet. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera två sidnummer i en sidnummerlista. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera en indexpost och dess sidnummer. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera början och slutet av ett sidintervall. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Hämtar eller anger om underposter ska köras på samma rad som huvudposten. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Hämtar eller anger namnet på en sekvens vars nummer ingår i sidnumret. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Hämtar eller anger om användning av yomi-text för indexposter ska aktiveras. |

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

Skapar ett index med hjälp av indexposterna som anges av XE-fält och infogar det indexet på denna plats i dokumentet.

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

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
