---
title: Document.Sections
linktitle: Sections
articleTitle: Sections
second_title: Aspose.Words for .NET
description: Explore the Document Sections property to access a complete collection of all document sections, enhancing your content organization and navigation.
type: docs
weight: 390
url: /net/aspose.words/document/sections/
---
## Document.Sections property

Returns a collection that represents all sections in the document.

```csharp
public SectionCollection Sections { get; }
```

## Examples

Shows how to add and remove sections in a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.That(doc.GetText().Trim(), Is.EqualTo("Section 1\x000cSection 2"));

// Delete the first section from the document.
doc.Sections.RemoveAt(0);

Assert.That(doc.GetText().Trim(), Is.EqualTo("Section 2"));

// Append a copy of what is now the first section to the end of the document.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.That(doc.GetText().Trim(), Is.EqualTo("Section 2\x000cSection 2"));
```

Shows how to specify how a new section separates itself from the previous.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Section break types determine how a new section separates itself from the previous section.
// Below are five types of section breaks.
// 1 -  Starts the next section on a new page:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.That(doc.Sections[1].PageSetup.SectionStart, Is.EqualTo(SectionStart.NewPage));

// 2 -  Starts the next section on the current page:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.That(doc.Sections[2].PageSetup.SectionStart, Is.EqualTo(SectionStart.Continuous));

// 3 -  Starts the next section on a new even page:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.That(doc.Sections[3].PageSetup.SectionStart, Is.EqualTo(SectionStart.EvenPage));

// 4 -  Starts the next section on a new odd page:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.That(doc.Sections[4].PageSetup.SectionStart, Is.EqualTo(SectionStart.OddPage));

// 5 -  Starts the next section on a new column:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.That(doc.Sections[5].PageSetup.SectionStart, Is.EqualTo(SectionStart.NewColumn));

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### See Also

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
