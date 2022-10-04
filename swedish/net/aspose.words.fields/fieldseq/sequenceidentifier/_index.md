---
title: SequenceIdentifier
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in namnet som tilldelas serien av objekt som ska numreras.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Hämtar eller ställer in namnet som tilldelas serien av objekt som ska numreras.

```csharp
public string SequenceIdentifier { get; set; }
```

### Exempel

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

* class [FieldSeq](../)
* namnutrymme [Aspose.Words.Fields](../../fieldseq/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
