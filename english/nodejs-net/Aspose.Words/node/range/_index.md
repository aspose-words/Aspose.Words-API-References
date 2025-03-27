---
title: Node.range property
linktitle: range property
articleTitle: range property
second_title: Aspose.Words for NodeJs
description: "Node.range property. Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words/node/range/
---

## Node.range property

Returns a [Range](../../range/) object that represents the portion of a document that is contained in this node.



```js
get range(): Aspose.Words.Range
```

### Examples

Shows how to delete all the nodes from a range.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add text to the first section in the document, and then add another section.
builder.write("Section 1. ");
builder.insertBreak(aw.BreakType.SectionBreakContinuous);
builder.write("Section 2.");

expect(doc.getText().trim()).toEqual("Section 1. \fSection 2.");

// Remove the first section entirely by removing all the nodes
// within its range, including the section itself.
doc.sections.at(0).range.delete();

expect(doc.sections.count).toEqual(1);
expect(doc.getText().trim()).toEqual("Section 2.");
```

### See Also

* module [Aspose.Words](../../)
* class [Node](../)

