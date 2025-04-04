---
title: Style.isQuickStyle property
linktitle: isQuickStyle property
articleTitle: isQuickStyle property
second_title: Aspose.Words for Node.js
description: "Style.isQuickStyle property. Specifies whether this style is shown in the Quick Style gallery inside MS Word UI."
type: docs
weight: 80
url: /nodejs-net/aspose.words/style/isQuickStyle/
---

## Style.isQuickStyle property

Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.


```js
get isQuickStyle(): boolean
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

