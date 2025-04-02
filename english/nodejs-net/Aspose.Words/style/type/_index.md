---
title: Style.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for NodeJs
description: "Style.type property. Gets the style type (paragraph or character)."
type: docs
weight: 200
url: /nodejs-net/Aspose.Words/style/type/
---

## Style.type property

Gets the style type (paragraph or character).


```js
get type(): Aspose.Words.StyleType
```

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

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

