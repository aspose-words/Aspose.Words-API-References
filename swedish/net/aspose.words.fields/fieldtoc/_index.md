---
title: FieldToc Class
linktitle: FieldToc
articleTitle: FieldToc
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldToc för sömlös skapande av innehållsförteckningar i dokument. Förbättra ditt arbetsflöde med kraftfulla funktioner!
type: docs
weight: 2940
url: /sv/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implementerar innehållsförteckningsfältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

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
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Hämtar eller anger namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Hämtar eller anger namnet på sekvensidentifieraren som används vid uppbyggnad av en figurtabell som inte inkluderar bildtextens etikett och nummer. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Hämtar eller ställer in en lista med andra stilar än de inbyggda rubrikstilarna som ska inkluderas i innehållsförteckningen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Hämtar eller anger en sträng som ska matcha typidentifierare för TC-fält som ingår. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Hämtar eller anger ett intervall av nivåer för innehållsförteckningsposter som ska inkluderas. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Hämtar eller anger en teckensekvens som separerar en post och dess sidnummer. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Hämtar eller ställer in ett intervall av rubriknivåer att inkludera. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Hämtar eller anger om tabbrad och sidnummer ska döljas i webblayoutvyn. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | Hämtar eller anger om innehållsförteckningens poster ska vara hyperlänkar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Hämtar eller anger ett intervall av nivåer i innehållsförteckningen från vilka sidnummer ska utelämnas. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Hämtar eller anger identifieraren för en sekvens för vilken ett prefix ska läggas till postens sidnummer. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Hämtar eller anger om nyradstecken ska bevaras i tabellposter. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Hämtar eller anger om tabbposter ska bevaras i tabellposter. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Hämtar eller anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Hämtar eller anger namnet på sekvensidentifieraren som används vid uppbyggnad av en figurtabell. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Hämtar eller anger om den tillämpade styckedispositionsnivån ska användas. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Uppdaterar sidnumren för objekt i innehållsförteckningen. |

## Anmärkningar

Skapar en innehållsförteckning (som också kan vara en figurförteckning) med hjälp av de poster som anges av TC-fält, deras rubriknivåer och angivna format, och infogar tabellen på denna plats i dokumentet.

## Exempel

Visar hur man infogar en innehållsförteckning och fyller den med poster baserat på rubrikformat.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Infoga ett innehållsförteckningsfält, vilket sammanställer alla rubriker till en innehållsförteckning.
    // För varje rubrik skapar det här fältet en rad med texten i den rubrikstilen till vänster,
    // och sidan där rubriken visas till höger.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Använd egenskapen BookmarkName för att endast lista rubriker
    // som visas inom gränserna för ett bokmärke med namnet "MittBokmärke".
    field.BookmarkName = "MyBookmark";

    // Text med en inbyggd rubrikstil, till exempel "Rubrik 1", räknas som en rubrik.
    // Vi kan namnge ytterligare stilar som ska hämtas som rubriker av innehållsförteckningen i den här egenskapen och deras innehållsförteckningsnivåer.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Som standard separeras nivåerna för stilar/innehållsförteckningar i egenskapen CustomStyles med ett kommatecken,
    // men vi kan ställa in en anpassad avgränsare i den här egenskapen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurera fältet för att exkludera rubriker som har innehållsförteckningsnivåer utanför detta intervall.
    field.HeadingLevelRange = "1-3";

    // Innehållsförteckningen visar inte sidnumren för rubriker vars innehållsförteckningsnivåer ligger inom detta intervall.
    field.PageNumberOmittingLevelRange = "2-5";

     // Ställ in en anpassad sträng som separerar varje rubrik från dess sidnummer.
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

    // Den här posten visas inte eftersom "Rubrik 4" ligger utanför intervallet "1-3" som vi ställde in tidigare.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Den här posten visas inte eftersom den ligger utanför bokmärket som anges i innehållsförteckningen.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Börja en ny sida och infoga ett stycke med en angiven stil.
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

Visar hur man fyller i ett innehållsförteckningsfält med poster med hjälp av sekvensfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett innehållsförteckningsfält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
// Varje post innehåller stycket som innehåller SEQ-fältet och sidans nummer där fältet visas.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata antal för varje unik namngiven sekvens
// identifierad av SEQ-fältets egenskap "SequenceIdentifier".
// Använd egenskapen "TableOfFiguresLabel" för att namnge en huvudsekvens för innehållsförteckningen.
// Nu kommer denna innehållsförteckning endast att skapa poster från SEQ-fält med deras "SequenceIdentifier" inställd på "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Vi kan namnge en annan SEQ-fältsekvens i egenskapen "PrefixedSequenceIdentifier".
 // SEQ-fält från denna prefixsekvens skapar inte innehållsförteckningsposter.
// Varje innehållsförteckningspost som skapas från ett huvudsekvens-SEQ-fält kommer nu också att visa antalet som
// prefixsekvensen är för närvarande aktiverad vid det primära sekvenssekvensfältet som gjorde posten.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Varje innehållsförteckning visar prefixsekvensantalet omedelbart till vänster
// av sidnumret där huvudsekvensens SEQ-fält visas på.
// Vi kan ange en anpassad avgränsare som ska visas mellan dessa två tal.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Det finns två sätt att använda SEQ-fält för att fylla i denna innehållsförteckning.
// 1 - Infogar ett SEQ-fält som tillhör prefixsekvensen för innehållsförteckningen:
// Det här fältet ökar antalet SEQ-sekvenser för "PrefixSequence" med 1.
// Eftersom detta fält inte tillhör den identifierade huvudsekvensen
// med egenskapen "TableOfFiguresLabel" i innehållsförteckningen kommer den inte att visas som en post.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Infogar ett SEQ-fält som tillhör innehållsförteckningens huvudsekvens:
// Detta SEQ-fält skapar en post i innehållsförteckningen.
// Innehållsförteckningen innehåller stycket där SEQ-fältet finns och sidnumret där det visas.
// Denna post visar också antalet prefixsekvenser som för närvarande har,
// separerat från sidnumret med värdet i innehållsförteckningens SeqenceSeparator-egenskap.
// Antalet "PrefixSequence" är 1, detta huvudsekvens-SEQ-fält finns på sidan 2,
// och avgränsaren är ">", så posten kommer att visa "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Infoga en sida, flytta prefixsekvensen med 2 och infoga ett SEQ-fält för att skapa en innehållsförteckningspost efteråt.
// Prefixsekvensen är nu 2, och huvudsekvensens SEQ-fält finns på sidan 3,
// så innehållsförteckningen visar "2>3" vid sidantal.
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
