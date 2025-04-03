---
title: Document.pageCount property
linktitle: pageCount property
articleTitle: pageCount property
second_title: Aspose.Words for NodeJs
description: "Document.pageCount property. Gets the number of pages in the document as calculated by the most recent page layout operation."
type: docs
weight: 310
url: /nodejs-net/aspose.words/document/pageCount/
---

## Document.pageCount property

Gets the number of pages in the document as calculated by the most recent page layout operation.


```js
get pageCount(): number
```

### Examples

Shows how to count the number of pages in the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.write("Page 1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.write("Page 2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.write("Page 3");
// Verify the expected page count of the document.
expect(doc.pageCount).toEqual(3);
// Getting the PageCount property invoked the document's page layout to calculate the value.
// This operation will not need to be re-done when rendering the document to a fixed page save format,
// such as .pdf. So you can save some time, especially with more complex documents.
doc.save(base.artifactsDir + "Document.GetPageCount.pdf");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)
* method [Document.updatePageLayout()](../updatePageLayout/#default)

