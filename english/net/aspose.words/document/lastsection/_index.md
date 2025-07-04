---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words for .NET
description: Discover the LastSection property to easily access the final section of your document, enhancing navigation and content management efficiency.
type: docs
weight: 250
url: /net/aspose.words/document/lastsection/
---
## Document.LastSection property

Gets the last section in the document.

```csharp
public Section LastSection { get; }
```

## Remarks

Returns `null` if there are no sections.

## Examples

Shows how to create a new section with a document builder.

```csharp
Document doc = new Document();

// A blank document contains one section by default,
// which contains child nodes that we can edit.
Assert.That(doc.Sections.Count, Is.EqualTo(1));

// Use a document builder to add text to the first section.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Create a second section by inserting a section break.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.That(doc.Sections.Count, Is.EqualTo(2));

// Each section has its own page setup settings.
// We can split the text in the second section into two columns.
// This will not affect the text in the first section.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.That(doc.FirstSection.PageSetup.TextColumns.Count, Is.EqualTo(1));
Assert.That(doc.LastSection.PageSetup.TextColumns.Count, Is.EqualTo(2));

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### See Also

* class [Section](../../section/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
