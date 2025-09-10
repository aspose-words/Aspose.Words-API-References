---
title: StyleCollection class
linktitle: StyleCollection class
articleTitle: StyleCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.StyleCollection class. A collection of [Style](../style/) objects that represent both the built-in and user-defined styles in a document"
type: docs
weight: 1270
url: /nodejs-net/aspose.words/stylecollection/
---

## StyleCollection class

A collection of [Style](../style/) objects that represent both the built-in and user-defined styles in a document.
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/nodejs-net/working-with-styles-and-themes/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of styles in the collection. |
| [defaultFont](./defaultFont/) | Gets document default text formatting. |
| [defaultParagraphFormat](./defaultParagraphFormat/) | Gets document default paragraph formatting. |
| [document](./document/) | Gets the owner document. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(type, name)](./add/#styletype_string) | Creates a new user defined style and adds it the collection. |
|[ addCopy(style)](./addCopy/#style) | Copies a style into this collection. |
|[ clearQuickStyleGallery()](./clearQuickStyleGallery/#default) | Removes all styles from the Quick Style Gallery panel. |

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

* module [Aspose.Words](../)

