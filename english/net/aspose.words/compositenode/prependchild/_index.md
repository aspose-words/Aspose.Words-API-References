---
title: CompositeNode.PrependChild
linktitle: PrependChild
articleTitle: PrependChild
second_title: Aspose.Words for .NET
description: Discover how the CompositeNode PrependChild method enhances your data structure by efficiently adding nodes to the start of your child node list.
type: docs
weight: 170
url: /net/aspose.words/compositenode/prependchild/
---
## CompositeNode.PrependChild&lt;T&gt; method

Adds the specified node to the beginning of the list of child nodes for this node.

```csharp
public T PrependChild<T>(T newChild)
    where T : Node
```

| Parameter | Type | Description |
| --- | --- | --- |
| newChild | T | The node to add. |

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
Assert.That(doc.FirstSection.Body.Paragraphs.Count, Is.EqualTo(1));

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
Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Initial text."));

// Insert the second run into the paragraph in front of the initial run.
paragraph.InsertBefore(run2, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text."));

// Insert the third run after the initial run.
paragraph.InsertAfter(run3, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text. Run 3."));

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.PrependChild(run1);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Run 2. Initial text. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(4));

// We can modify the contents of the run by editing and deleting existing child nodes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Updated run 2. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(3));
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
