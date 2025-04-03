---
title: Style.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for NodeJs
description: "Style.font property. Gets the character formatting of the style."
type: docs
weight: 60
url: /nodejs-net/aspose.words/style/font/
---

## Style.font property

Gets the character formatting of the style.


```js
get font(): Aspose.Words.Font
```

### Remarks

For list styles this property returns ``null``.




### Examples

Shows how to create and apply a custom style.

```js
let doc = new aw.Document();

let style = doc.styles.add(aw.StyleType.Paragraph, "MyStyle");
style.font.name = "Times New Roman";
style.font.size = 16;
style.font.color = "#000080";
// Automatically redefine style.
style.automaticallyUpdate = true;

let builder = new aw.DocumentBuilder(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder.paragraphFormat.style = doc.styles.at("MyStyle");
builder.writeln("Hello world!");

let firstParagraphStyle = doc.firstSection.body.firstParagraph.paragraphFormat.style;

expect(firstParagraphStyle).toEqual(style);

// Remove our custom style from the document's styles collection.
doc.styles.at("MyStyle").remove();

firstParagraphStyle = doc.firstSection.body.firstParagraph.paragraphFormat.style;

// Any text that used a removed style reverts to the default formatting.
expect([...doc.styles].every(s => s.name == "MyStyle")).toEqual(false);
expect(firstParagraphStyle.font.name).toEqual("Times New Roman");
expect(firstParagraphStyle.font.size).toEqual(12.0);
expect(firstParagraphStyle.font.color).toEqual(base.emptyColor);
```

Shows how to create and use a paragraph style with list formatting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a custom paragraph style.
let style = doc.styles.add(aw.StyleType.Paragraph, "MyStyle1");
style.font.size = 24;
style.font.name = "Verdana";
style.paragraphFormat.spaceAfter = 12;

// Create a list and make sure the paragraphs that use this style will use this list.
style.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);
style.listFormat.listLevelNumber = 0;

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.paragraphFormat.style = style;
builder.writeln("Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder.paragraphFormat.style = doc.styles.at("Normal");
builder.writeln("Hello World: Normal.");

builder.document.save(base.artifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

