---
title: NodeList class
linktitle: NodeList class
articleTitle: NodeList class
second_title: Aspose.Words for Python
description: "aspose.words.NodeList class. Represents a collection of nodes matching an XPath query executed using the [CompositeNode.select_nodes()](../compositenode/select_nodes/#str) method"
type: docs
weight: 830
url: /python-net/aspose.words/nodelist/
---

## NodeList class

Represents a collection of nodes matching an XPath query executed using the [CompositeNode.select_nodes()](../compositenode/select_nodes/#str) method.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

[NodeList](./) is returned by [CompositeNode.select_nodes()](../compositenode/select_nodes/#str) and contains a collection
of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.

> **NOTE**
>
> Treat the [NodeList](./) collection as a "snapshot" collection. [NodeList](./) starts
> as a "live" collection because the nodes are not actually retrieved when the XPath query is run.
> The nodes are only retrieved upon access and at this time the node and all nodes that precede
> it are cached forming a "snapshot" collection.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a node at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of nodes in the list. |

### Methods

| Name | Description |
| --- | --- |
|[ to_array()](./to_array/#default) | Copies all nodes from the collection to a new array of nodes. |

### See Also

* module [aspose.words](../)

