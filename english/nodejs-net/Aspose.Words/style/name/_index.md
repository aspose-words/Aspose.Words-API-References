---
title: Style.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "Style.name property. Gets or sets the name of the style."
type: docs
weight: 130
url: /nodejs-net/aspose.words/style/name/
---

## Style.name property

Gets or sets the name of the style.


```js
get name(): string
```

### Remarks

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.




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

Shows how to clone a document's style.

```js
let doc = new aw.Document();

// The AddCopy method creates a copy of the specified style and
// automatically generates a new name for the style, such as "Heading 1_0".
let newStyle = doc.styles.addCopy(doc.styles.at("Heading 1"));

// Use the style's "Name" property to change the style's identifying name.
newStyle.name = "My Heading 1";

// Our document now has two identical looking styles with different names.
// Changing settings of one of the styles do not affect the other.
newStyle.font.color = "#FF0000";

expect(newStyle.name).toEqual("My Heading 1");
expect(doc.styles.at("Heading 1").name).toEqual("Heading 1");

expect(newStyle.type).toEqual(doc.styles.at("Heading 1").type);
expect(newStyle.font.name).toEqual(doc.styles.at("Heading 1").font.name);
expect(newStyle.font.size).toEqual(doc.styles.at("Heading 1").font.size);
expect(newStyle.font.color).not.toEqual(doc.styles.at("Heading 1").font.color);
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

