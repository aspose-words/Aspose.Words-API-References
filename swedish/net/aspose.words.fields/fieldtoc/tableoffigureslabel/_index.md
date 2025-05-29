---
title: FieldToc.TableOfFiguresLabel
linktitle: TableOfFiguresLabel
articleTitle: TableOfFiguresLabel
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldToc TableOfFiguresLabel för att enkelt anpassa din figurtabell. Förbättra dokumentets organisation och tydlighet!
type: docs
weight: 160
url: /sv/net/aspose.words.fields/fieldtoc/tableoffigureslabel/
---
## FieldToc.TableOfFiguresLabel property

Hämtar eller anger namnet på sekvensidentifieraren som används vid uppbyggnad av en figurtabell.

```csharp
public string TableOfFiguresLabel { get; set; }
```

## Exempel

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

* class [FieldToc](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
