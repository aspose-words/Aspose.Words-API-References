---
title: TxtLoadOptions.detectNumberingWithWhitespaces property
linktitle: detectNumberingWithWhitespaces property
articleTitle: detectNumberingWithWhitespaces property
second_title: Aspose.Words for NodeJs
description: "TxtLoadOptions.detectNumberingWithWhitespaces property. Allows to specify how numbered list items are recognized when document is imported from plain text format"
type: docs
weight: 40
url: /nodejs-net/aspose.words.loading/txtloadoptions/detectNumberingWithWhitespaces/
---

## TxtLoadOptions.detectNumberingWithWhitespaces property

Allows to specify how numbered list items are recognized when document is imported from plain text format.
The default value is ``true``.


```js
get detectNumberingWithWhitespaces(): boolean
```

### Remarks

If this option is set to ``false``, lists recognition algorithm detects list paragraphs, when list numbers ends with
either dot, right bracket or bullet symbols (such as "•", "\*", "-" or "o").

If this option is set to ``true``, whitespaces are also used as list number delimiters:
list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.




### Examples

Shows how to detect lists when loading plaintext documents.

```js
// Create a plaintext document in a string with four separate parts that we may interpret as lists,
// with different delimiters. Upon loading the plaintext document into a "Document" object,
// Aspose.words will always detect the first three lists and will add a "List" object
// for each to the document's "Lists" property.
const textDoc = "Full stop delimiters:\n" +
          "1. First list item 1\n" +
          "2. First list item 2\n" +
          "3. First list item 3\n\n" +
          "Right bracket delimiters:\n" +
          "1) Second list item 1\n" +
          "2) Second list item 2\n" +
          "3) Second list item 3\n\n" +
          "Bullet delimiters:\n" +
          "• Third list item 1\n" +
          "• Third list item 2\n" +
          "• Third list item 3\n\n" +
          "Whitespace delimiters:\n" +
          "1 Fourth list item 1\n" +
          "2 Fourth list item 2\n" +
          "3 Fourth list item 3";

// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
let loadOptions = new aw.Loading.TxtLoadOptions();

// Set the "DetectNumberingWithWhitespaces" property to "true" to detect numbered items
// with whitespace delimiters, such as the fourth list in our document, as lists.
// This may also falsely detect paragraphs that begin with numbers as lists.
// Set the "DetectNumberingWithWhitespaces" property to "false"
// to not create lists from numbered items with whitespace delimiters.
loadOptions.detectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

let doc = new aw.Document(Buffer.from(textDoc), loadOptions);

if (detectNumberingWithWhitespaces)
{
  expect(doc.lists.count).toEqual(4);
  expect(doc.firstSection.body.paragraphs.toArray().some(p => p.getText().includes("Fourth list") && p.isListItem)).toEqual(true);
}
else
{
  expect(doc.lists.count).toEqual(3);
  expect(doc.firstSection.body.paragraphs.toArray().some(p => p.getText().includes("Fourth list") && p.isListItem)).toEqual(false);
}
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [TxtLoadOptions](../)

