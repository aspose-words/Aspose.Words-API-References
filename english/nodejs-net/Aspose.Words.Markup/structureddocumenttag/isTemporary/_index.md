---
title: StructuredDocumentTag.isTemporary property
linktitle: isTemporary property
articleTitle: isTemporary property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTag.isTemporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /nodejs-net/aspose.words.markup/structureddocumenttag/isTemporary/
---

## StructuredDocumentTag.isTemporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```js
get isTemporary(): boolean
```

### Examples

Shows how to make single-use controls.

```js
let doc = new aw.Document();

// Insert a plain text structured document tag,
// which will act as a plain text form that the user may enter text into.
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);

// Set the "IsTemporary" property to "true" to make the structured document tag disappear and
// assimilate its contents into the document after the user edits it once in Microsoft Word.
// Set the "IsTemporary" property to "false" to allow the user to edit the contents
// of the structured document tag any number of times.
tag.isTemporary = isTemporary;

let builder = new aw.DocumentBuilder(doc);
builder.write("Please enter text: ");
builder.insertNode(tag);

// Insert another structured document tag in the form of a check box and set its default state to "checked".
tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.Checkbox, aw.Markup.MarkupLevel.Inline);
tag.checked = true;

// Set the "IsTemporary" property to "true" to make the check box become a symbol
// once the user clicks on it in Microsoft Word.
// Set the "IsTemporary" property to "false" to allow the user to click on the check box any number of times.
tag.isTemporary = isTemporary;

builder.write("\nPlease click the check box: ");
builder.insertNode(tag);

doc.save(base.artifactsDir + "StructuredDocumentTag.isTemporary.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

