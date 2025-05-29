---
title: FieldSeq.ResetHeadingLevel
linktitle: ResetHeadingLevel
articleTitle: ResetHeadingLevel
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldSeq ResetHeadingLevel, hantera enkelt rubriknivåer genom att återställa sekvensnummer. Förenkla din dokumentformatering idag!
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

### Se även

* class [FieldSeq](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
