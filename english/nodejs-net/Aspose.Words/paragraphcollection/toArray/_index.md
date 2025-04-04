---
title: ParagraphCollection.toArray method
linktitle: toArray method
articleTitle: toArray method
second_title: Aspose.Words for Node.js
description: "ParagraphCollection.toArray method. Copies all paragraphs from the collection to a new array of paragraphs."
type: docs
weight: 10
url: /nodejs-net/aspose.words/paragraphcollection/toArray/
---

## toArray() {#default}

Copies all paragraphs from the collection to a new array of paragraphs.


```js
toArray()
```

### Returns

An array of paragraphs.


### Examples

Shows how to create an array from a NodeCollection.

```js
let doc = new aw.Document(base.myDir + "Paragraphs.docx");

let paras = doc.firstSection.body.paragraphs.toArray();

expect(paras.length).toEqual(22);
```

Shows how to use "hot remove" to remove a node during enumeration.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("The first paragraph");
builder.writeln("The second paragraph");
builder.writeln("The third paragraph");
builder.writeln("The fourth paragraph");

// Remove a node from the collection in the middle of an enumeration.
for (var para of doc.firstSection.body.paragraphs.toArray())
  if (para.range.text.includes("third"))
    para.remove();

expect(doc.getText().includes("The third paragraph")).toEqual(false);
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphCollection](../)

