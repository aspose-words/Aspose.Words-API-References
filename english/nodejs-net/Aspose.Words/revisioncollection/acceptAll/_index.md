---
title: RevisionCollection.acceptAll method
linktitle: acceptAll method
articleTitle: acceptAll method
second_title: Aspose.Words for NodeJs
description: "RevisionCollection.acceptAll method. Accepts all revisions in this collection."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/revisioncollection/acceptAll/
---

## acceptAll() {#default}

Accepts all revisions in this collection.


```js
acceptAll()
```

### Examples

Shows how to compare documents.

```js
let docOriginal = new aw.Document();
let builder = new aw.DocumentBuilder(docOriginal);
builder.writeln("This is the original document.");

let docEdited = new aw.Document();
builder = new aw.DocumentBuilder(docEdited);
builder.writeln("This is the edited document.");

// Comparing documents with revisions will throw an exception.
if (docOriginal.revisions.count == 0 && docEdited.revisions.count == 0)
  docOriginal.compare(docEdited, "authorName", Date.now());

// After the comparison, the original document will gain a new revision
// for every element that is different in the edited document.
expect(docOriginal.revisions.count).toEqual(2);
for (let r of docOriginal.revisions)
{
  console.log(`Revision type: ${r.revisionType}, on a node of type \"${r.parentNode.nodeType}\"`);
  console.log(`\tChanged text: \"${r.parentNode.getText()}\"`);
}

// Accepting these revisions will transform the original document into the edited document.
docOriginal.revisions.acceptAll();

expect(docEdited.getText()).toEqual(docOriginal.getText());
```

### See Also

* module [Aspose.Words](../../)
* class [RevisionCollection](../)

