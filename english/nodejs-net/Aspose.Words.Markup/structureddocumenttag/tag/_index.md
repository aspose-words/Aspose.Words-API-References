﻿---
title: StructuredDocumentTag.tag property
linktitle: tag property
articleTitle: tag property
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.tag property. Specifies a tag associated with the current SDT node"
type: docs
weight: 280
url: /nodejs-net/aspose.words.markup/structureddocumenttag/tag/
---

## StructuredDocumentTag.tag property

Specifies a tag associated with the current SDT node.
Can not be ``null``.



```js
get tag(): string
```

### Remarks

A tag is an arbitrary string which applications can associate with SDT
in order to identify it without providing a visible friendly name.


### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```js
let doc = new aw.Document();

// Create a structured document tag that will contain plain text.
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);

// Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
tag.title = "My plain text";
tag.color = "#FF00FF";

// Set a tag for this structured document tag, which is obtainable
// as an XML element named "tag", with the string below in its "@val" attribute.
tag.tag = "MyPlainTextSDT";

// Every structured document tag has a random unique ID.
expect(tag.id > 0).toEqual(true);

// Set the font for the text inside the structured document tag.
tag.contentsFont.name = "Arial";

// Set the font for the text at the end of the structured document tag.
// Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
tag.endCharacterFont.name = "Arial Black";

// By default, this is false and pressing enter while inside a structured document tag does nothing.
// When set to true, our structured document tag can have multiple lines.

// Set the "Multiline" property to "false" to only allow the contents
// of this structured document tag to span a single line.
// Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
tag.multiline = true;

// Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
// By default structured document tag shows as BoundingBox. 
tag.appearance = aw.Markup.SdtAppearance.Tags;

let builder = new aw.DocumentBuilder(doc);
builder.insertNode(tag);

// Insert a clone of our structured document tag in a new paragraph.
let tagClone = tag.clone(true).asStructuredDocumentTag();
builder.insertParagraph();
builder.insertNode(tagClone);

// Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
tagClone.removeSelfOnly();

doc.save(base.artifactsDir + "StructuredDocumentTag.plainText.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

