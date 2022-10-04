---
title: FieldToc
second_title: Aspose.Words för .NET API Referens
description: Implementerar TOCfältet.
type: docs
weight: 2380
url: /sv/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implementerar TOC-fältet.

```csharp
public class FieldToc : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldToc](fieldtoc/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Hämtar eller ställer in namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Hämtar eller ställer in namnet på sekvensidentifieraren som används när man bygger en tabell med figurer som inte inkluderar bildtextens etikett och nummer. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Hämtar eller ställer in en lista över andra stilar än de inbyggda rubrikstilarna som ska inkluderas i innehållsförteckningen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Hämtar eller ställer in en sträng som ska matcha typidentifierare för TC-fält som ingår. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Hämtar eller ställer in ett intervall av nivåer i innehållsförteckningen som ska inkluderas. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Hämtar eller ställer in en sekvens av tecken som separerar en post och dess sidnummer. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Hämtar eller ställer in ett intervall av rubriknivåer som ska inkluderas. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Hämtar eller ställer in om flikledare och sidnummer ska döljas i webblayoutvyn. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | Hämtar eller ställer in om innehållsförteckningsposterna ska vara hyperlänkar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Hämtar eller ställer in ett intervall av nivåer i innehållsförteckningsposterna för att utelämna sidnummer. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Hämtar eller ställer in identifieraren för en sekvens för vilken ett prefix ska läggas till i postens sidnummer. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Hämtar eller ställer in om nyradstecken ska bevaras i tabellposter. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Hämtar eller ställer in om flikposter ska bevaras i tabellposter. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Hämtar eller ställer in teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Hämtar eller ställer in namnet på sekvensidentifieraren som används när man bygger en tabell med figurer. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Hämtar eller ställer in om den tillämpade styckekonturnivån ska användas. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Uppdaterar sidnumren för objekt i den här innehållsförteckningen. |

### Anmärkningar

Bygger en innehållsförteckning (som också kan vara en figurförteckning) med hjälp av de poster som anges av TC-fält, deras rubriknivåer och specificerade stilar, och infogar den tabellen på denna plats i dokumentet.

### Exempel

Visar hur man infogar en innehållsförteckning och fyller den med poster baserat på rubrikstilar.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Infoga ett innehållsförteckning-fält, som kommer att kompilera alla rubriker till en innehållsförteckning.
    // För varje rubrik kommer det här fältet att skapa en rad med texten i den rubrikstilen till vänster,
    // och sidan rubriken visas till höger.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Använd egenskapen BookmarkName för att bara lista rubriker
    // som visas inom gränserna för ett bokmärke med namnet "Mitt bokmärke".
    field.BookmarkName = "MyBookmark";

    // Text med en inbyggd rubrikstil, till exempel "Rubrik 1", som tillämpas på den kommer att räknas som en rubrik.
    // Vi kan namnge ytterligare stilar som ska plockas upp som rubriker av innehållsförteckningen i den här egenskapen och deras innehållsförteckningsnivåer.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Som standard är Styles/TOC-nivåer separerade i CustomStyles-egenskapen med ett kommatecken,
    // men vi kan ställa in en anpassad avgränsare i den här egenskapen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurera fältet för att utesluta alla rubriker som har innehållsförteckningsnivåer utanför detta intervall.
    field.HeadingLevelRange = "1-3";

    // Innehållsförteckningen visar inte sidnumren för rubriker vars innehållsförteckningsnivåer ligger inom detta intervall.
    field.PageNumberOmittingLevelRange = "2-5";

      // Ställ in en anpassad sträng som skiljer varje rubrik från dess sidnummer.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Dessa två rubriker kommer att ha sidnumren utelämnade eftersom de ligger inom intervallet "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Den här posten visas inte eftersom "Rubrik 4" ligger utanför intervallet "1-3" som vi har ställt in tidigare.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Den här posten visas inte eftersom den ligger utanför bokmärket som anges av innehållsförteckningen.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");

/// <summary>
/// Starta en ny sida och infoga ett stycke av en angiven stil.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

Visar hur man fyller i ett innehållsförteckningsfält med poster med hjälp av SEQ-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett TOC-fält kan skapa en post i dess innehållsförteckning för varje SEQ-fält som finns i dokumentet.
// Varje post innehåller stycket som innehåller SEQ-fältet och sidans nummer som fältet visas på.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata räkningar för varje unik namngiven sekvens
// identifieras av SEQ-fältets "SequenceIdentifier"-egenskap.
// Använd egenskapen "TableOfFiguresLabel" för att namnge en huvudsekvens för innehållsförteckningen.
// Nu kommer denna innehållsförteckning endast att skapa poster från SEQ-fält med deras "SequenceIdentifier" inställd på "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Vi kan namnge en annan SEQ-fältsekvens i egenskapen "PrefixedSequenceIdentifier".
  // SEQ-fält från denna prefixsekvens kommer inte att skapa TOC-poster.
// Varje TOC-post som skapas från ett SEQ-fält i huvudsekvensen kommer nu också att visa antalet som
// Prefixsekvensen är för närvarande på i det primära sekvens SEQ-fältet som gjorde inmatningen.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Varje TOC-post kommer att visa prefixsekvensräkningen omedelbart till vänster
// av sidnumret som SEQ-fältet för huvudsekvensen visas på.
// Vi kan ange en anpassad avgränsare som kommer att visas mellan dessa två siffror.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Det finns två sätt att använda SEQ-fält för att fylla i denna innehållsförteckning.
// 1 - Infoga ett SEQ-fält som hör till innehållsförteckningens prefixsekvens:
// Detta fält kommer att öka antalet SEQ-sekvenser för "PrefixSequence" med 1.
// Eftersom detta fält inte tillhör den identifierade huvudsekvensen
// av egenskapen "TableOfFiguresLabel" för innehållsförteckningen, kommer den inte att visas som en post.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Infoga ett SEQ-fält som hör till innehållsförteckningens huvudsekvens:
// Detta SEQ-fält kommer att skapa en post i innehållsförteckningen.
// TOC-posten kommer att innehålla stycket som SEQ-fältet finns i och numret på sidan som det visas på.
// Den här posten visar också antalet som prefixsekvensen för närvarande är på,
// separerat från sidnumret med värdet i TOC:s SeqenceSeparator-egenskap.
// Antalet "PrefixSequence" är 1, detta SEQ-fält för huvudsekvensen finns på sidan 2,
// och avgränsaren är ">", så posten kommer att visa "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Infoga en sida, flytta prefixsekvensen med 2 och infoga ett SEQ-fält för att skapa en TOC-post efteråt.
// Prefixsekvensen är nu på 2, och huvudsekvensens SEQ-fält finns på sidan 3,
// så TOC-posten kommer att visa "2>3" vid sitt antal sidor.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
