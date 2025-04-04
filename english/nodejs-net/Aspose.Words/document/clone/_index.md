---
title: Document.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Node.js
description: "Document.clone method. Performs a deep copy of the [Document](../)."
type: docs
weight: 570
url: /nodejs-net/aspose.words/document/clone/
---

## clone() {#default}

Performs a deep copy of the [Document](../).



```js
clone()
```

### Returns

The cloned document.


### Examples

Shows how to deep clone a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.write("Hello world!");
// Cloning will produce a new document with the same contents as the original,
// but with a unique copy of each of the original document's nodes.
let clone = doc.clone();
expect(doc.firstSection.body.firstParagraph.runs.at(0).getText()).toEqual(
    clone.firstSection.body.firstParagraph.runs.at(0).text);
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

