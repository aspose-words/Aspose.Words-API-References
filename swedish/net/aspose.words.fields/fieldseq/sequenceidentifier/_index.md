---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldSeq SequenceIdentifier för att enkelt hantera och anpassa artikelserienamn för effektiv numrering och organisation.
type: docs
weight: 60
url: /sv/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Hämtar eller anger namnet som tilldelats serien av objekt som ska numreras.

```csharp
public string SequenceIdentifier { get; set; }
```

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

* class [FieldSeq](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
