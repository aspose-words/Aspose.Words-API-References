﻿---
title: CompositeNode.lastChild property
linktitle: lastChild property
articleTitle: lastChild property
second_title: Aspose.Words for Node.js
description: "CompositeNode.lastChild property. Gets the last child of the node."
type: docs
weight: 50
url: /nodejs-net/aspose.words/compositenode/lastChild/
---

## CompositeNode.lastChild property

Gets the last child of the node.


```js
get lastChild(): Aspose.Words.Node
```

### Remarks

If there is no last child node, a ``null`` is returned.



### Examples

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Section 1 text.");
builder.insertBreak(aw.BreakType.SectionBreakContinuous);
builder.writeln("Section 2 text.");

// Both sections are siblings of each other.
let lastSection = doc.lastChild.asSection();
let firstSection = lastSection.previousSibling.asSection();

// Remove a section based on its sibling relationship with another section.
if (lastSection.previousSibling != null)
  doc.removeChild(firstSection);

// The section we removed was the first one, leaving the document with only the second.
expect(doc.getText().trim()).toEqual("Section 2 text.");
```

### See Also

* module [Aspose.Words](../../)
* class [CompositeNode](../)

