---
title: DocumentBuilder.pushFont method
linktitle: pushFont method
articleTitle: pushFont method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.pushFont method. Saves current character formatting onto the stack."
type: docs
weight: 640
url: /nodejs-net/aspose.words/documentbuilder/pushFont/
---

## pushFont() {#default}

Saves current character formatting onto the stack.


```js
pushFont()
```

### Examples

Shows how to use a document builder's formatting stack.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Set up font formatting, then write the text that goes before the hyperlink.
builder.font.name = "Arial";
builder.font.size = 24;
builder.write("To visit Google, hold Ctrl and click ");

// Preserve our current formatting configuration on the stack.
builder.pushFont();

// Alter the builder's current formatting by applying a new style.
builder.font.styleIdentifier = aw.StyleIdentifier.Hyperlink;
builder.insertHyperlink("here", "http://www.google.com", false);

expect(builder.font.color).toEqual("#0000FF");
expect(builder.font.underline).toEqual(aw.Underline.Single);

// Restore the font formatting that we saved earlier and remove the element from the stack.
builder.popFont();

expect(builder.font.color).toEqual(base.emptyColor);
expect(builder.font.underline).toEqual(aw.Underline.None);

builder.write(". We hope you enjoyed the example.");

doc.save(base.artifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)
* property [DocumentBuilder.font](../font/)
* method [DocumentBuilder.popFont()](../popFont/#default)

