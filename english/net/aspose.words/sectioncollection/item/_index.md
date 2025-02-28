---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access specific sections effortlessly with the SectionCollection Item property. Retrieve any section by index for streamlined data management.
type: docs
weight: 10
url: /net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Retrieves a section at the given index.

```csharp
public Section this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | An index into the list of sections. |

## Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples

Shows when to recalculate the page layout of the document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// In the current version of Aspose.Words, modifying the document does not automatically rebuild
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

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

* class [Section](../../section/)
* class [SectionCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
