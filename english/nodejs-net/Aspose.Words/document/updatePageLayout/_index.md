---
title: Document.updatePageLayout method
linktitle: updatePageLayout method
articleTitle: updatePageLayout method
second_title: Aspose.Words for NodeJs
description: "Document.updatePageLayout method. Rebuilds the page layout of the document."
type: docs
weight: 780
url: /nodejs-net/Aspose.Words/document/updatePageLayout/
---

## updatePageLayout() {#default}

Rebuilds the page layout of the document.


```js
updatePageLayout()
```

### Remarks

This method formats a document into pages and updates the page number related fields in the document such
as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document
to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it.
However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not
update the page layout automatically. In this case you should call [Document.updatePageLayout()](./#default) before
rendering again.




### See Also

* module [Aspose.Words](../../)
* class [Document](../)

