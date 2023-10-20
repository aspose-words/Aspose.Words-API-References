---
title: FieldSeq.ResetHeadingLevel
linktitle: ResetHeadingLevel
articleTitle: ResetHeadingLevel
second_title: Aspose.Words för .NET
description: FieldSeq ResetHeadingLevel fast egendom. Hämtar eller ställer in ett heltal som representerar en rubriknivå för att återställa sekvensnumret till. Returnerar 1 om talet saknas i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldseq/resetheadinglevel/
---
## FieldSeq.ResetHeadingLevel property

Hämtar eller ställer in ett heltal som representerar en rubriknivå för att återställa sekvensnumret till. Returnerar -1 om talet saknas.

```csharp
public string ResetHeadingLevel { get; set; }
```

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

### Se även

* class [FieldSeq](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
