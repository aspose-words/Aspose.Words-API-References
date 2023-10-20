---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.FieldSeq klass. Implementerar SEQfältet i C#.
type: docs
weight: 2390
url: /sv/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implementerar SEQ-fältet.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

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
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Hämtar eller ställer in ett bokmärkesnamn som refererar till ett objekt någon annanstans i dokumentet snarare än på den aktuella platsen. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Hämtar eller ställer in om nästa sekvensnummer för det angivna objektet ska infogas. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Hämtar eller ställer in ett heltal som representerar en rubriknivå för att återställa sekvensnumret till. Returnerar -1 om talet saknas. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Hämtar eller ställer in ett heltal att återställa sekvensnumret till. Returnerar -1 om numret saknas. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Hämtar eller ställer in namnet som tilldelas serien av objekt som ska numreras. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

## Anmärkningar

Räknar kapitel, tabeller, figurer och andra användardefinierade listor över objekt i ett dokument i följd.

## Exempel

Visar skapa numrering med SEQ-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata räkningar för varje unik namngiven sekvens
// identifieras av SEQ-fältets "SequenceIdentifier"-egenskap.
// Infoga ett SEQ-fält som visar det aktuella räknevärdet för "MySequence",
// efter att ha använt egenskapen "ResetNumber" för att ställa in den till 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Visa nästa nummer i denna sekvens med ett annat SEQ-fält.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Infoga en nivå 1-rubrik.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Infoga ett annat SEQ-fält från samma sekvens och konfigurera det för att återställa räkningen vid varje rubrik med 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Ovanstående rubrik är en nivå 1-rubrik, så räkningen för denna sekvens återställs till 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Flytta till nästa nummer i denna sekvens.
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

Visar hur man kombinerar innehållsförteckning och sekvensfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ett TOC-fält kan skapa en post i dess innehållsförteckning för varje SEQ-fält som finns i dokumentet.
// Varje post innehåller stycket som innehåller SEQ-fältet,
// och numret på sidan som fältet visas på.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Konfigurera detta TOC-fält så att det har en SequenceIdentifier-egenskap med värdet "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Konfigurera detta innehållsförteckningsfält för att bara ta upp SEQ-fält som ligger inom gränserna för ett bokmärke
// heter "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ-fält visar ett antal som ökar vid varje SEQ-fält.
// Dessa fält har också separata räkningar för varje unik namngiven sekvens
// identifieras av SEQ-fältets "SequenceIdentifier"-egenskap.
// Infoga ett SEQ-fält som har en sekvensidentifierare som matchar innehållsförteckningarna
// TableOfFiguresLabel-egenskap. Detta fält kommer inte att skapa en post i innehållsförteckningen eftersom det är utanför
// bokmärkets gränser angivna av "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Detta SEQ-fälts sekvens matchar innehållsförteckningens "TableOfFiguresLabel"-egenskap och är inom bokmärkets gränser.
// Stycket som innehåller detta fält kommer att visas i innehållsförteckningen som en post.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Detta SEQ-fälts sekvens matchar inte innehållsförteckningens "TableOfFiguresLabel"-egenskap,
// och är inom gränserna för bokmärket. Dess stycke kommer inte att visas i innehållsförteckningen som en post.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Detta SEQ-fälts sekvens matchar innehållsförteckningens "TableOfFiguresLabel"-egenskap och ligger inom bokmärkets gränser.
// Detta fält refererar också till ett annat bokmärke. Innehållet i det bokmärket kommer att visas i TOC-posten för detta SEQ-fält.
// Själva SEQ-fältet visar inte innehållet i det bokmärket.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Skapa ett bokmärke med innehåll som kommer att dyka upp i TOC-posten på grund av att ovanstående SEQ-fält refererar till det.
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
