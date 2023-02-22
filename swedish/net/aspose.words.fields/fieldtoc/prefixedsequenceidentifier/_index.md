---
title: FieldToc.PrefixedSequenceIdentifier
second_title: Aspose.Words för .NET API Referens
description: FieldToc fast egendom. Hämtar eller ställer in identifieraren för en sekvens för vilken ett prefix ska läggas till i postens sidnummer.
type: docs
weight: 120
url: /sv/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

Hämtar eller ställer in identifieraren för en sekvens för vilken ett prefix ska läggas till i postens sidnummer.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

### Exempel

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

* class [FieldToc](../)
* namnutrymme [Aspose.Words.Fields](../../fieldtoc/)
* hopsättning [Aspose.Words](../../../)


