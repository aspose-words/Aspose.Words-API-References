---
title: LayoutCollector.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Node.js
description: "LayoutCollector.document property. Gets or sets the document this collector instance is attached to."
type: docs
weight: 20
url: /nodejs-net/aspose.words.layout/layoutcollector/document/
---

## LayoutCollector.document property

Gets or sets the document this collector instance is attached to.


```js
get document(): Aspose.Words.Document
```

### Remarks

If you need to access page indexes of the document nodes you need to set this property to point to a document instance,
before page layout of the document is built. It is best to set this property to ``null`` afterwards, 
otherwise the collector continues to accumulate information from subsequent rebuilds of the document's page layout.



### See Also

* module [Aspose.Words.Layout](../../)
* class [LayoutCollector](../)

