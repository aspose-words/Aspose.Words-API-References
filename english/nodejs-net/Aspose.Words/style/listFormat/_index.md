---
title: Style.listFormat property
linktitle: listFormat property
articleTitle: listFormat property
second_title: Aspose.Words for NodeJs
description: "Style.listFormat property. Provides access to the list formatting properties of a paragraph style."
type: docs
weight: 110
url: /nodejs-net/Aspose.Words/style/listFormat/
---

## Style.listFormat property

Provides access to the list formatting properties of a paragraph style.


```js
get listFormat(): Aspose.Words.Lists.ListFormat
```

### Remarks

This property is only valid for paragraph styles.
For other style types this property returns ``None``.




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

