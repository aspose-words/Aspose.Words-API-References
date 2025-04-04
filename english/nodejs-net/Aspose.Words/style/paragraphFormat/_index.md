---
title: Style.paragraphFormat property
linktitle: paragraphFormat property
articleTitle: paragraphFormat property
second_title: Aspose.Words for Node.js
description: "Style.paragraphFormat property. Gets the paragraph formatting of the style."
type: docs
weight: 150
url: /nodejs-net/aspose.words/style/paragraphFormat/
---

## Style.paragraphFormat property

Gets the paragraph formatting of the style.


```js
get paragraphFormat(): Aspose.Words.ParagraphFormat
```

### Remarks

For character and list styles this property returns ``null``.




### Examples

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

