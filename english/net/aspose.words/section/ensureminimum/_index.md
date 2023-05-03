---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
second_title: Aspose.Words for .NET API Reference
description: Section EnsureMinimum method. Ensures that the section has Body with one Paragraph in C#.
type: docs
weight: 130
url: /net/aspose.words/section/ensureminimum/
---
## EnsureMinimum method

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
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// If we add a new section like this, it will not have a body, or any other child nodes.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../section/)
* assembly [Aspose.Words](../../../)
