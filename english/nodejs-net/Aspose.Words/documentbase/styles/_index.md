---
title: DocumentBase.styles property
linktitle: styles property
articleTitle: styles property
second_title: Aspose.Words for Node.js
description: "DocumentBase.styles property. Returns a collection of styles defined in the document."
type: docs
weight: 90
url: /nodejs-net/aspose.words/documentbase/styles/
---

## DocumentBase.styles property

Returns a collection of styles defined in the document.


```js
get styles(): Aspose.Words.StyleCollection
```

### Remarks

For more information see the description of the [StyleCollection](../../stylecollection/) class.




### Examples

Shows how to access a document's style collection.

```js
let doc = new aw.Document();

expect(doc.styles.count).toEqual(4);

// Enumerate and list all the styles that a document created using Aspose.words contains by default.
for (var style of doc.styles)
{
  console.log(`Style name:\t\"${style.name}\", of type \"${style.type}\"`);
  console.log(`\tSubsequent style:\t${style.nextParagraphStyleName}`);
  console.log(`\tIs heading:\t\t\t${style.isHeading}`);
  console.log(`\tIs QuickStyle:\t\t${style.isQuickStyle}`);

  expect(style.document.referenceEquals(doc)).toBe(true);
}
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
* class [DocumentBase](../)
* class [StyleCollection](../../stylecollection/)
* class [Style](../../style/)

