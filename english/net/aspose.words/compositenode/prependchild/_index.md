---
title: CompositeNode.PrependChild
linktitle: PrependChild
articleTitle: PrependChild
second_title: Aspose.Words for .NET
description: CompositeNode PrependChild method. Adds the specified node to the beginning of the list of child nodes for this node in C#.
type: docs
weight: 160
url: /net/aspose.words/compositenode/prependchild/
---
## CompositeNode.PrependChild method

Adds the specified node to the beginning of the list of child nodes for this node.

```csharp
public Node PrependChild(Node newChild)
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | Node | The node to add. |

### Return Value

The node added.

## Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [`ImportNode`](../../documentbase/importnode/) to import the node to the current document. The imported node can then be inserted into the current document.

## Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```csharp
Document doc = new Document();

// An empty document, by default, has one paragraph.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Create three more run nodes.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Insert the second run into the paragraph in front of the initial run.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insert the third run after the initial run.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// We can modify the contents of the run by editing and deleting existing child nodes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
