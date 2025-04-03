---
title: Style.nextParagraphStyleName property
linktitle: nextParagraphStyleName property
articleTitle: nextParagraphStyleName property
second_title: Aspose.Words for NodeJs
description: "Style.nextParagraphStyleName property. Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style."
type: docs
weight: 140
url: /nodejs-net/aspose.words/style/nextParagraphStyleName/
---

## Style.nextParagraphStyleName property

Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a
paragraph formatted with the specified style.


```js
get nextParagraphStyleName(): string
```

### Remarks

This property is not used by Aspose.Words. The next paragraph style will only
be applied automatically when you edit the document in MS Word.


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

