---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words for .NET
description: Discover how the CompositeNode IndexOf method efficiently locates the index of a specified child node in the array, enhancing your coding experience.
type: docs
weight: 140
url: /net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Returns the index of the specified child node in the child node array.

```csharp
public int IndexOf(Node child)
```

## Remarks

Returns -1 if the node is not found in the child nodes.

## Examples

Shows how to get the index of a given child node from its parent.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Retrieve the index of the last paragraph in the body of the first section.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### See Also

* class [Node](../../node/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
