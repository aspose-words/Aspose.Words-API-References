---
title: DocumentBase.warningCallback property
linktitle: warningCallback property
articleTitle: warningCallback property
second_title: Aspose.Words for Node.js
description: "DocumentBase.warningCallback property. Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss."
type: docs
weight: 100
url: /nodejs-net/aspose.words/documentbase/warningCallback/
---

## DocumentBase.warningCallback property

Called during various document processing procedures when an issue is detected that might result
in data or formatting fidelity loss.


```js
get warningCallback(): Aspose.Words.IWarningCallback
```

### Remarks

Document may generate warnings at any stage of its existence, so it's important to setup warning callback as
early as possible to avoid the warnings loss. E.g. such properties as [Document.pageCount](../../document/pageCount/)
actually build the document layout which is used later for rendering, and the layout warnings may be lost if
warning callback is specified just for the rendering calls later.



### See Also

* module [Aspose.Words](../../)
* class [DocumentBase](../)

