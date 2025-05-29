---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldSeq för sömlös implementering av SEQ-fält. Förbättra din dokumentautomation med kraftfulla funktioner och flexibilitet.
type: docs
weight: 2800
url: /sv/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implementerar SEQ-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldSeq : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldSeq](fieldseq/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Hämtar eller anger ett bokmärkesnamn som refererar till ett objekt någon annanstans i dokumentet snarare än på den aktuella platsen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Hämtar eller anger om nästa sekvensnummer ska infogas för det angivna objektet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Hämtar eller ställer in ett heltal som representerar en rubriknivå för att återställa sekvensnumret till. Returnerar -1 om talet saknas. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Hämtar eller ställer in ett heltal att återställa sekvensnumret till. Returnerar -1 om talet saknas. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Hämtar eller anger namnet som tilldelats serien av objekt som ska numreras. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

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

Numrerar kapitel, tabeller, figurer och andra användardefinierade listor över objekt i ett dokument sekventiellt.

## Exempel

Visar skapande av numrering med hjälp av SEQ-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata antal för varje unik namngiven sekvens
// identifierad av SEQ-fältets egenskap "SequenceIdentifier".
// Infoga ett SEQ-fält som visar det aktuella räknevärdet för "MySequence",
// efter att ha använt egenskapen "ResetNumber" för att ställa in den till 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Visa nästa tal i den här sekvensen med ett annat SEQ-fält.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Infoga en rubrik på nivå 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Infoga ett annat SEQ-fält från samma sekvens och konfigurera det så att det återställer räknaren vid varje rubrik med 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Rubriken ovan är en rubrik på nivå 1, så räknaren för denna sekvens återställs till 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Gå till nästa nummer i den här sekvensen.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Visar hur man kombinerar innehållsförtecknings- och sekvensfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett innehållsförteckningsfält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
// Varje post innehåller stycket som innehåller SEQ-fältet,
// och numret på sidan där fältet visas.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurera detta innehållsförteckningsfält så att det har en SequenceIdentifier-egenskap med värdet "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Konfigurera detta innehållsförteckningsfält för att endast hämta SEQ-fält som ligger inom gränserna för ett bokmärke
// med namnet "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata antal för varje unik namngiven sekvens
// identifierad av SEQ-fältets egenskap "SequenceIdentifier".
// Infoga ett SEQ-fält som har en sekvensidentifierare som matchar innehållsförteckningen
// egenskapen TableOfFiguresLabel. Det här fältet skapar inte en post i innehållsförteckningen eftersom det ligger utanför
// bokmärkets gränser angivna av "Bokmärkesnamn".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Sekvensen i detta SEQ-fält matchar egenskapen "TableOfFiguresLabel" i innehållsförteckningen och ligger inom bokmärkets gränser.
// Stycket som innehåller det här fältet kommer att visas i innehållsförteckningen som en post.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Sekvensen i detta SEQ-fält matchar inte egenskapen "TableOfFiguresLabel" i innehållsförteckningen.
// och ligger inom bokmärkets gränser. Dess stycke kommer inte att visas i innehållsförteckningen som en post.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Sekvensen i detta SEQ-fält matchar egenskapen "TableOfFiguresLabel" i innehållsförteckningen och ligger inom bokmärkets gränser.
// Detta fält refererar också till ett annat bokmärke. Innehållet i det bokmärket kommer att visas i innehållsförteckningen för detta sekvensfält.
// Själva SEQ-fältet visar inte innehållet i det bokmärket.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Skapa ett bokmärke med innehåll som visas i innehållsförteckningen på grund av att ovanstående SEQ-fält refererar till det.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
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
