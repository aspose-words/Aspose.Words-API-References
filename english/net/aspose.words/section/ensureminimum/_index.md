---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Optimize your content with the EnsureMinimum method, guaranteeing each section includes a Body with a Paragraph for enhanced clarity and structure.
type: docs
weight: 150
url: /net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Ensures that the section has [`Body`](../body/) with one [`Paragraph`](../../paragraph/).

```csharp
public void EnsureMinimum()
```

## Examples

Shows how to prepare a new section node for editing.

```csharp
Document doc = new Document();

// A blank document comes with a section, which has a body, which in turn has a paragraph.
// We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
Assert.That(doc.GetChild(NodeType.Any, 0, true).NodeType, Is.EqualTo(NodeType.Section));
Assert.That(doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType, Is.EqualTo(NodeType.Body));
Assert.That(doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType, Is.EqualTo(NodeType.Paragraph));

// If we add a new section like this, it will not have a body, or any other child nodes.
doc.Sections.Add(new Section(doc));

Assert.That(doc.Sections[1].GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(0));

// Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
doc.LastSection.EnsureMinimum();

Assert.That(doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType, Is.EqualTo(NodeType.Body));
Assert.That(doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType, Is.EqualTo(NodeType.Paragraph));

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
