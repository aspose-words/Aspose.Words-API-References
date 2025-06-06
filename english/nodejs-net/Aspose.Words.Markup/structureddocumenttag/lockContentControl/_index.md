﻿---
title: StructuredDocumentTag.lockContentControl property
linktitle: lockContentControl property
articleTitle: lockContentControl property
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.lockContentControl property. When set to ``true``, this property will prohibit a user from deleting this SDT."
type: docs
weight: 190
url: /nodejs-net/aspose.words.markup/structureddocumenttag/lockContentControl/
---

## StructuredDocumentTag.lockContentControl property

When set to ``true``, this property will prohibit a user from deleting this **SDT**.



```js
get lockContentControl(): boolean
```

### Examples

Shows how to apply editing restrictions to structured document tags.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);

// Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
tag.lockContents = true;
builder.write("The contents of this structured document tag cannot be edited: ");
builder.insertNode(tag);

tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);

// Set the "LockContentControl" property to "true" to prohibit the user from
// deleting this structured document tag manually in Microsoft Word.
tag.lockContentControl = true;

builder.insertParagraph();
builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.insertNode(tag);

doc.save(base.artifactsDir + "StructuredDocumentTag.Lock.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

