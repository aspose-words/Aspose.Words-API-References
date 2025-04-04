---
title: Section constructor
linktitle: Section constructor
articleTitle: Section constructor
second_title: Aspose.Words for Node.js
description: "Section constructor. Initializes a new instance of the Section class."
type: docs
weight: 10
url: /nodejs-net/aspose.words/section/constructor/
---

## Section(doc) {#documentbase}

Initializes a new instance of the Section class.


```js
Section(doc: Aspose.Words.DocumentBase)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When the section is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../node/parentNode/) is ``null``.

To include [Section](../) into a document use [CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node) and 
[CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node) methods of the [Document](../../document/) OR
[NodeCollection.add()](../../nodecollection/add/#node) and [NodeCollection.insert()](../../nodecollection/insert/#number_node) methods of the [Document.sections](../../document/sections/) property.




### See Also

* module [Aspose.Words](../../)
* class [Section](../)

