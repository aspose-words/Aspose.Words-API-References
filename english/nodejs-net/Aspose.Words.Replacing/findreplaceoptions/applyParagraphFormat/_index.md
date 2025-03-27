---
title: FindReplaceOptions.applyParagraphFormat property
linktitle: applyParagraphFormat property
articleTitle: applyParagraphFormat property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.applyParagraphFormat property. Paragraph formatting applied to new content."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/applyParagraphFormat/
---

## FindReplaceOptions.applyParagraphFormat property

Paragraph formatting applied to new content.


```js
get applyParagraphFormat(): Aspose.Words.ParagraphFormat
```

### Examples

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.writeln("This one will not!");
builder.write("This one also will.");

let paragraphs = doc.firstSection.body.paragraphs.toArray();

expect(paragraphs.at(0).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(1).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(2).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// that contains a match that the find-and-replace operation finds.
options.applyParagraphFormat.alignment = aw.ParagraphAlignment.Right;

// Replace every full stop that is right before a paragraph break with an exclamation point.
var count = doc.range.replace(".&p", "!&p", options);

expect(count).toEqual(2);
paragraphs = doc.firstSection.body.paragraphs.toArray();
expect(paragraphs.at(0).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
expect(paragraphs.at(1).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(2).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
expect(doc.getText().trim()).toEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                        "This one will not!\r" +
                        "This one also will!");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

