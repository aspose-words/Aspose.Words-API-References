---
title: HeaderFooter constructor
linktitle: HeaderFooter constructor
articleTitle: HeaderFooter constructor
second_title: Aspose.Words for Node.js
description: "HeaderFooter constructor. Creates a new header or footer of the specified type."
type: docs
weight: 10
url: /nodejs-net/aspose.words/headerfooter/constructor/
---

## HeaderFooter(doc, headerFooterType) {#documentbase_headerfootertype}

Creates a new header or footer of the specified type.


```js
HeaderFooter(doc: Aspose.Words.DocumentBase, headerFooterType: Aspose.Words.HeaderFooterType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |
| headerFooterType | [HeaderFooterType](../../headerfootertype/) | A [HeaderFooter.headerFooterType](../headerFooterType/) value that specifies the type of the header or footer. |

### Remarks

When [HeaderFooter](../) is created, it belongs to the specified document, but is not
yet part of the document and [Node.parentNode](../../node/parentNode/) is ``null``.

To append [HeaderFooter](../) to a [Section](../../section/) use [CompositeNode.insertAfter()](../../compositenode/insertAfter/#node_node), [CompositeNode.insertBefore()](../../compositenode/insertBefore/#node_node),
or [Section.headersFooters](../../section/headersFooters/) property and methods [NodeCollection.add()](../../nodecollection/add/#node), [NodeCollection.insert()](../../nodecollection/insert/#number_node).




### See Also

* module [Aspose.Words](../../)
* class [HeaderFooter](../)

