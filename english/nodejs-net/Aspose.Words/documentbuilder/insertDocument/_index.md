---
title: DocumentBuilder.insertDocument method
linktitle: insertDocument method
articleTitle: insertDocument method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertDocument method"
type: docs
weight: 310
url: /nodejs-net/Aspose.Words/documentbuilder/insertDocument/
---

## insertDocument(srcDoc, importFormatMode) {#document_importformatmode}

Inserts a document at the cursor position.


```js
insertDocument(srcDoc: Aspose.Words.DocumentimportFormatMode: Aspose.Words.ImportFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../document/) | Source document for inserting. |
| importFormatMode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

### Remarks

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed,
then CTRL+'C' (copy selected into the buffer) inside one document
and then CTRL+'V' (insert content from the buffer) inside another document.


### Returns

First node of the inserted content.


## insertDocument(srcDoc, importFormatMode, importFormatOptions) {#document_importformatmode_importformatoptions}

Inserts a document at the cursor position.


```js
insertDocument(srcDoc: Aspose.Words.DocumentimportFormatMode: Aspose.Words.ImportFormatModeimportFormatOptions: Aspose.Words.ImportFormatOptions)
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


### Returns

First node of the inserted content.


## Examples

Shows how to insert a document into another document.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let builder = new aw.DocumentBuilder(doc);
builder.moveToDocumentEnd();
builder.insertBreak(aw.BreakType.PageBreak);

let docToInsert = new aw.Document(base.myDir + "Formatted elements.docx");

builder.insertDocument(docToInsert, aw.ImportFormatMode.KeepSourceFormatting);
builder.document.save(base.artifactsDir + "DocumentBuilder.insertDocument.docx");
```

Shows how to resolve duplicate styles while inserting documents.

```js
let dstDoc = new aw.Document();
let builder = new aw.DocumentBuilder(dstDoc);

let myStyle = builder.document.styles.add(aw.StyleType.Paragraph, "MyStyle");
myStyle.font.size = 14;
myStyle.font.name = "Courier New";
myStyle.font.color = "#0000FF";

builder.paragraphFormat.styleName = myStyle.name;
builder.writeln("Hello world!");

// Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
// If we insert the clone into the original document, the two styles with the same name will cause a clash.
let srcDoc = dstDoc.clone(); // TODO cast to Document
srcDoc.styles.at("MyStyle").font.color = "#FF0000";

// When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
// Aspose.words will resolve style clashes by converting source document styles.
// with the same names as destination styles into direct paragraph attributes.
let options = new aw.ImportFormatOptions();
options.smartStyleBehavior = true;

builder.insertDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting, options);

dstDoc.save(base.artifactsDir + "DocumentBuilder.smartStyleBehavior.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

