---
title: Style.isHeading property
linktitle: isHeading property
articleTitle: isHeading property
second_title: Aspose.Words for Node.js
description: "Style.isHeading property. True when the style is one of the built-in Heading styles."
type: docs
weight: 70
url: /nodejs-net/aspose.words/style/isHeading/
---

## Style.isHeading property

True when the style is one of the built-in Heading styles.


```js
get isHeading(): boolean
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

