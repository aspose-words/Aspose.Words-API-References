---
title: DocumentBuilder.insertParagraph method
linktitle: insertParagraph method
articleTitle: insertParagraph method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.insertParagraph method. Inserts a paragraph break into the document."
type: docs
weight: 450
url: /nodejs-net/Aspose.Words/documentbuilder/insertParagraph/
---

## insertParagraph() {#default}

Inserts a paragraph break into the document.


```js
insertParagraph()
```

### Remarks

Current paragraph formatting specified by the [DocumentBuilder.paragraphFormat](../paragraphFormat/) property is used.

Breaks the current paragraph in two. After inserting the paragraph, the cursor is placed at the beginning of the new paragraph.

An exception is thrown if it is not possible to insert a paragraph break at the current cursor position.




### Returns

The paragraph node that was just inserted. It is the same node as [DocumentBuilder.currentParagraph](../currentParagraph/).


### Examples

Shows how to insert a paragraph into the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let font = builder.font;
font.size = 16;
font.bold = true;
font.color = "#0000FF";
font.name = "Arial";
font.underline = aw.Underline.Dash;

let paragraphFormat = builder.paragraphFormat;
paragraphFormat.firstLineIndent = 8;
paragraphFormat.alignment = aw.ParagraphAlignment.Justify;
paragraphFormat.addSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.addSpaceBetweenFarEastAndDigit = true;
paragraphFormat.keepTogether = true;

// The "Writeln" method ends the paragraph after appending text
// and then starts a new line, adding a new paragraph.
builder.writeln("Hello world!");

expect(builder.currentParagraph.isEndOfDocument).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

