---
title: DocumentBuilder.insertHyperlink method
linktitle: insertHyperlink method
articleTitle: insertHyperlink method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.insertHyperlink method. Inserts a hyperlink into the document."
type: docs
weight: 390
url: /nodejs-net/Aspose.Words/documentbuilder/insertHyperlink/
---

## insertHyperlink(displayText, urlOrBookmark, isBookmark) {#string_string_boolean}

Inserts a hyperlink into the document.


```js
insertHyperlink(displayText: stringurlOrBookmark: stringisBookmark: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| displayText | string | Text of the link to be displayed in the document. |
| urlOrBookmark | string | Link destination. Can be a url or a name of a bookmark inside the document. This method always adds apostrophes at the beginning and end of the url. |
| isBookmark | boolean | ``True`` if the previous parameter is a name of a bookmark inside the document; ``False`` is the previous parameter is a URL. |

### Remarks

Note that you need to specify font formatting for the hyperlink display text explicitly
using the [DocumentBuilder.font](../font/) property.

This methods internally calls [DocumentBuilder.insertField()](../insertField/#string) to insert an MS Word HYPERLINK field
into the document.




### Returns

A [Field](../../field/) object that represents the inserted field.


### Examples

Shows how to insert a hyperlink field.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("For more information, please visit the ");

// Insert a hyperlink and emphasize it with custom formatting.
// The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = "#0000FF";
builder.font.underline = aw.Underline.Single;
builder.insertHyperlink("Google website", "https://www.google.com", false);
builder.font.clearFormatting();
builder.writeln(".");

// Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(base.artifactsDir + "DocumentBuilder.insertHyperlink.docx");
```

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

Shows how to insert a hyperlink which references a local bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startBookmark("Bookmark1");
builder.write("Bookmarked text. ");
builder.endBookmark("Bookmark1");
builder.writeln("Text outside of the bookmark.");

// Insert a HYPERLINK field that links to the bookmark. We can pass field switches
// to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
builder.font.color = "#0000FF";
builder.font.underline = aw.Underline.Single;
let hyperlink = builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true).asFieldHyperlink();
hyperlink.screenTip = "Hyperlink Tip";

doc.save(base.artifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

