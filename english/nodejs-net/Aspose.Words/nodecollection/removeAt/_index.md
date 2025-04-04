---
title: NodeCollection.removeAt method
linktitle: removeAt method
articleTitle: removeAt method
second_title: Aspose.Words for Node.js
description: "NodeCollection.removeAt method. Removes the node at the specified index from the collection and from the document."
type: docs
weight: 90
url: /nodejs-net/aspose.words/nodecollection/removeAt/
---

## removeAt(index) {#number}

Removes the node at the specified index from the collection and from the document.


```js
removeAt(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

### Examples

Shows how to add and remove sections in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 2");

expect(doc.getText().trim()).toEqual("Section 1\u000cSection 2");

// Delete the first section from the document.
doc.sections.removeAt(0);

expect(doc.getText().trim()).toEqual("Section 2");

// Append a copy of what is now the first section to the end of the document.
let lastSectionIdx = doc.sections.count - 1;
let newSection = doc.sections.at(lastSectionIdx).clone();
doc.sections.add(newSection);

expect(doc.getText().trim()).toEqual("Section 2\u000cSection 2");
```

### See Also

* module [Aspose.Words](../../)
* class [NodeCollection](../)

