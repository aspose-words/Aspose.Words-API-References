---
title: Body constructor
linktitle: Body constructor
articleTitle: Body constructor
second_title: Aspose.Words for NodeJs
description: "Body constructor. Initializes a new instance of the [Body](../) class."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/body/constructor/
---

## Body(doc) {#documentbase}

Initializes a new instance of the [Body](../) class.



```js
Body(doc: Aspose.Words.DocumentBase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Body](../) is created, it belongs to the specified document, but is not 
yet part of the document and [Node.parentNode](../../node/parentNode/) is ``null``.

To append [Body](../) to a [Section](../../section/) use [CompositeNode.appendChild()](../../compositenode/appendChild/#node)
[CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node) or [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node)
methods.




### See Also

* module [Aspose.Words](../../)
* class [Body](../)

