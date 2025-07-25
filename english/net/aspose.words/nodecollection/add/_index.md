---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: Discover the NodeCollection Add method to effortlessly append nodes to your collection, enhancing your data management with ease and efficiency.
type: docs
weight: 30
url: /net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Adds a node to the end of the collection.

```csharp
public void Add(Node node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | Node | The node to be added to the end of the collection. |

### Exceptions

| exception | condition |
| --- | --- |
| NotSupportedException | The [`NodeCollection`](../) is a "deep" collection. |

## Remarks

The node is inserted as a child into the node object from which the collection was created.

If the node being inserted was created from another document, you should use [`ImportNode`](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.

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

* class [Node](../../node/)
* class [NodeCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
