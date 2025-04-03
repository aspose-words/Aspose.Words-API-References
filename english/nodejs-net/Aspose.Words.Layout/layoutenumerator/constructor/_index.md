---
title: LayoutEnumerator constructor
linktitle: LayoutEnumerator constructor
articleTitle: LayoutEnumerator constructor
second_title: Aspose.Words for NodeJs
description: "LayoutEnumerator constructor. Initializes new instance of this class."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Layout/layoutenumerator/constructor/
---

## LayoutEnumerator(document) {#document}

Initializes new instance of this class.


```js
LayoutEnumerator(document: Aspose.Words.Document)
```

| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../../aspose.words/document/) | A document whose page layout model to enumerate. |

### Remarks

If page layout model of the document hasn't been built the enumerator calls [Document.updatePageLayout()](../../../aspose.words/document/updatePageLayout/#default) to build it.

Whenever document is updated and new page layout model is created, a new enumerator must be used to access it.




### See Also

* module [Aspose.Words.Layout](../../)
* class [LayoutEnumerator](../)

