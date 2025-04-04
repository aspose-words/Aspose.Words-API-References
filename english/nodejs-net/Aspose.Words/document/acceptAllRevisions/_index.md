---
title: Document.acceptAllRevisions method
linktitle: acceptAllRevisions method
articleTitle: acceptAllRevisions method
second_title: Aspose.Words for Node.js
description: "Document.acceptAllRevisions method. Accepts all tracked changes in the document."
type: docs
weight: 520
url: /nodejs-net/aspose.words/document/acceptAllRevisions/
---

## acceptAllRevisions() {#default}

Accepts all tracked changes in the document.


```js
acceptAllRevisions()
```

### Remarks

This method is a shortcut for [RevisionCollection.acceptAll()](../../revisioncollection/acceptAll/#default).


### Examples

Shows how to accept all tracking changes in the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Edit the document while tracking changes to create a few revisions.
doc.startTrackRevisions("John Doe");
builder.write("Hello world! ");
builder.write("Hello again! ");
builder.write("This is another revision.");
doc.stopTrackRevisions();

expect(doc.revisions.count).toEqual(3);

// We can iterate through every revision and accept/reject it as a part of our document.
// If we know we wish to accept every revision, we can do it more straightforwardly so by calling this method.
doc.acceptAllRevisions();

expect(doc.revisions.count).toEqual(0);
expect(doc.getText().trim()).toEqual("Hello world! Hello again! This is another revision.");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

