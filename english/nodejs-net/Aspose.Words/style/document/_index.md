---
title: Style.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for NodeJs
description: "Style.document property. Gets the owner document."
type: docs
weight: 50
url: /nodejs-net/aspose.words/style/document/
---

## Style.document property

Gets the owner document.


```js
get document(): Aspose.Words.DocumentBase
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

