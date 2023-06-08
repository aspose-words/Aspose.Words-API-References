---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Node Clone method. Creates a duplicate of the node in C#.
type: docs
weight: 100
url: /net/aspose.words/node/clone/
---
## Node.Clone method

Creates a duplicate of the node.

```csharp
public Node Clone(bool isCloneChildren)
```

| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | Boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

### Return Value

The cloned node.

## Remarks

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

## Examples

Shows how to clone a composite node.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Below are two ways of cloning a composite node.
// 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 -  Create a clone of a node just by itself without any children.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### See Also

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
