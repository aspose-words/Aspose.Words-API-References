---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: Aspose.Words for .NET
description: Discover the FieldSeq SequenceIdentifier property to effortlessly manage and customize item series names for efficient numbering and organization.
type: docs
weight: 60
url: /net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Gets or sets the name assigned to the series of items that are to be numbered.

```csharp
public string SequenceIdentifier { get; set; }
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

Shows how to populate a TOC field with entries using SEQ fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A TOC field can create an entry in its table of contents for each SEQ field found in the document.
// Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ fields display a count that increments at each SEQ field.
// These fields also maintain separate counts for each unique named sequence
// identified by the SEQ field's "SequenceIdentifier" property.
// Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
// Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
// SEQ fields from this prefix sequence will not create TOC entries. 
// Every TOC entry created from a main sequence SEQ field will now also display the count that
// the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Each TOC entry will display the prefix sequence count immediately to the left
// of the page number that the main sequence SEQ field appears on.
// We can specify a custom separator that will appear between these two numbers.
fieldToc.SequenceSeparator = ">";

Assert.That(fieldToc.GetFieldCode(), Is.EqualTo(" TOC  \\c MySequence \\s PrefixSequence \\d >"));

builder.InsertBreak(BreakType.PageBreak);

// There are two ways of using SEQ fields to populate this TOC.
// 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
// This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
// Since this field does not belong to the main sequence identified
// by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.That(fieldSeq.GetFieldCode(), Is.EqualTo(" SEQ  PrefixSequence"));

// 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
// This SEQ field will create an entry in the TOC.
// The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
// This entry will also display the count that the prefix sequence is currently at,
// separated from the page number by the value in the TOC's SeqenceSeparator property.
// The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
// and the separator is ">", so entry will display "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.That(fieldSeq.GetFieldCode(), Is.EqualTo(" SEQ  MySequence"));

// Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
// The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
// so the TOC entry will display "2>3" at its page count.
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

### See Also

* class [FieldSeq](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
