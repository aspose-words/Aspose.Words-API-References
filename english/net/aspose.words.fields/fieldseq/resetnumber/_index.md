---
title: FieldSeq.ResetNumber
linktitle: ResetNumber
articleTitle: ResetNumber
second_title: Aspose.Words for .NET
description: Manage your FieldSeq ResetNumber property effortlessly! Set or retrieve an integer to control sequence numbers, ensuring accurate data handling.
type: docs
weight: 50
url: /net/aspose.words.fields/fieldseq/resetnumber/
---
## FieldSeq.ResetNumber property

Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent.

```csharp
public string ResetNumber { get; set; }
```

## Examples

Shows create numbering using SEQ fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Insert a SEQ field that will display the current count value of "MySequence",
// after using the "ResetNumber" property to set it to 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.That(fieldSeq.GetFieldCode(), Is.EqualTo(" SEQ  MySequence \\r 100"));
Assert.That(fieldSeq.Result, Is.EqualTo("100"));

// Display the next number in this sequence with another SEQ field.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.That(fieldSeq.Result, Is.EqualTo("101"));

// Insert a level 1 heading.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// The above heading is a level 1 heading, so the count for this sequence is reset to 1.
Assert.That(fieldSeq.GetFieldCode(), Is.EqualTo(" SEQ  MySequence \\s 1"));
Assert.That(fieldSeq.Result, Is.EqualTo("1"));

// Move to the next number of this sequence.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.That(fieldSeq.GetFieldCode(), Is.EqualTo(" SEQ  MySequence \\n"));
Assert.That(fieldSeq.Result, Is.EqualTo("2"));

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

### See Also

* class [FieldSeq](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
