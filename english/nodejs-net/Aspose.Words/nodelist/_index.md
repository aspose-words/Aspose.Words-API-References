---
title: NodeList class
linktitle: NodeList class
articleTitle: NodeList class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.NodeList class. Represents a collection of nodes matching an XPath query executed using the [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) method"
type: docs
weight: 860
url: /nodejs-net/aspose.words/nodelist/
---

## NodeList class

Represents a collection of nodes matching an XPath query executed using the [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) method.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

[NodeList](./) is returned by [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) and contains a collection
of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.

> **NOTE**
>
> Treat the [NodeList](./) collection as a "snapshot" collection. [NodeList](./) starts
> as a "live" collection because the nodes are not actually retrieved when the XPath query is run.
> The nodes are only retrieved upon access and at this time the node and all nodes that precede
> it are cached forming a "snapshot" collection.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of nodes in the list. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ toArray()](./toArray/#default) | Copies all nodes from the collection to a new array of nodes. |

### See Also

* module [Aspose.Words](../)

