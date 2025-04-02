---
title: DocumentBuilder.insertStyleSeparator method
linktitle: insertStyleSeparator method
articleTitle: insertStyleSeparator method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.insertStyleSeparator method. Inserts style separator into the document."
type: docs
weight: 490
url: /nodejs-net/Aspose.Words/documentbuilder/insertStyleSeparator/
---

## insertStyleSeparator() {#default}

Inserts style separator into the document.


```js
insertStyleSeparator()
```

### Remarks

This method allows to apply different paragraph styles to two different parts of a text line.


### Examples

Shows how to work with style separators.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Each paragraph can only have one style.
// The InsertStyleSeparator method allows us to work around this limitation.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.write("This text is in a Heading style. ");
builder.insertStyleSeparator();

let paraStyle = builder.document.styles.add(aw.StyleType.Paragraph, "MyParaStyle");
paraStyle.font.bold = false;
paraStyle.font.size = 8;
paraStyle.font.name = "Arial";

builder.paragraphFormat.styleName = paraStyle.name;
builder.write("This text is in a custom style. ");

// Calling the InsertStyleSeparator method creates another paragraph,
// which can have a different style to the previous. There will be no break between paragraphs.
// The text in the output document will look like one paragraph with two styles.
expect(doc.firstSection.body.paragraphs.count).toEqual(2);
expect(doc.firstSection.body.paragraphs.at(0).paragraphFormat.style.name).toEqual("Heading 1");
expect(doc.firstSection.body.paragraphs.at(1).paragraphFormat.style.name).toEqual("MyParaStyle");

doc.save(base.artifactsDir + "DocumentBuilder.insertStyleSeparator.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

