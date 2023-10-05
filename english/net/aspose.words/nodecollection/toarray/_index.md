---
title: NodeCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words for .NET
description: NodeCollection ToArray method. Copies all nodes from the collection to a new array of nodes in C#.
type: docs
weight: 110
url: /net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Copies all nodes from the collection to a new array of nodes.

```csharp
public Node[] ToArray()
```

### Return Value

An array of nodes.

## Remarks

You should not be adding/removing nodes while iterating over a collection of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy nodes into a fixed-size array and then iterate over the array.

### See Also

* class [Node](../../node/)
* class [NodeCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
