---
title: DocumentBuilder.insertStructuredDocumentTag method
linktitle: insertStructuredDocumentTag method
articleTitle: insertStructuredDocumentTag method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertStructuredDocumentTag method. Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document."
type: docs
weight: 480
url: /nodejs-net/aspose.words/documentbuilder/insertStructuredDocumentTag/
---

## insertStructuredDocumentTag(type) {#sdttype}

Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document.



```js
insertStructuredDocumentTag(type: Aspose.Words.Markup.SdtType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [SdtType](../../../aspose.words.markup/sdttype/) |  |

### Returns

The [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node that was just inserted.


### Examples

Shows how to simply insert structured document tag.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");
let builder = new aw.DocumentBuilder(doc);

builder.moveTo(doc.firstSection.body.paragraphs.at(3));
// Note, that only following StructuredDocumentTag types are allowed for insertion:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.date.
// Markup level of inserted StructuredDocumentTag will be detected automatically and depends on position being inserted at.
// Added StructuredDocumentTag will inherit paragraph and font formatting from cursor position.
let sdtPlain = builder.insertStructuredDocumentTag(aw.Markup.SdtType.PlainText);

doc.save(base.artifactsDir + "StructuredDocumentTag.insertStructuredDocumentTag.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

