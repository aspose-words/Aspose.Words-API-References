---
title: DocumentBuilder.insertDocumentInline method
linktitle: insertDocumentInline method
articleTitle: insertDocumentInline method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertDocumentInline method. Inserts a document inline at the cursor position."
type: docs
weight: 320
url: /nodejs-net/aspose.words/documentbuilder/insertDocumentInline/
---

## insertDocumentInline(srcDoc, importFormatMode, importFormatOptions) {#document_importformatmode_importformatoptions}

Inserts a document inline at the cursor position.


```js
insertDocumentInline(srcDoc: Aspose.Words.Document, importFormatMode: Aspose.Words.ImportFormatMode, importFormatOptions: Aspose.Words.ImportFormatOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../document/) | Source document for inserting. |
| importFormatMode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| importFormatOptions | [ImportFormatOptions](../../importformatoptions/) | Allows to specify options that affect formatting of a result document. |

### Remarks

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed,
then CTRL+'C' (copy selected into the buffer) inside one document
and then CTRL+'V' (insert content from the buffer) inside another document.

As a difference from [DocumentBuilder.insertDocument()](../insertDocument/#document_importformatmode_importformatoptions)
this method moves the content of the paragraph of the destination document,
before which the source document is inserted, into the last
paragraph of the inserted source document. Actually, this means that
paragraph break of the last inserted paragraph is removed.

Note, if the last node of the source document is not a paragraph, then nothing will be done.




### Returns

First node of the inserted content.


### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

