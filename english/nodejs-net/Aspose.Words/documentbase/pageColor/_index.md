---
title: DocumentBase.pageColor property
linktitle: pageColor property
articleTitle: pageColor property
second_title: Aspose.Words for Node.js
description: "DocumentBase.pageColor property. Gets or sets the page color of the document"
type: docs
weight: 70
url: /nodejs-net/aspose.words/documentbase/pageColor/
---

## DocumentBase.pageColor property

Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.backgroundShape](../backgroundShape/).



```js
get pageColor(): string
```

### Remarks

This property provides a simple way to specify a solid page color for the document.
Setting this property creates and sets an appropriate [DocumentBase.backgroundShape](../backgroundShape/).

If the page color is not set (e.g. there is no background shape in the document) returns
.




### Examples

Shows how to set the background color for all pages of a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

doc.pageColor = "#D3D3D3";

doc.save(base.artifactsDir + "DocumentBase.SetPageColor.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBase](../)
* property [DocumentBase.backgroundShape](../backgroundShape/)

