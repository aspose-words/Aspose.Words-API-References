---
title: Body.ensureMinimum method
linktitle: ensureMinimum method
articleTitle: ensureMinimum method
second_title: Aspose.Words for NodeJs
description: "Body.ensureMinimum method. If the last child is not a paragraph, creates and appends one empty paragraph."
type: docs
weight: 70
url: /nodejs-net/aspose.words/body/ensureMinimum/
---

## ensureMinimum() {#default}

If the last child is not a paragraph, creates and appends one empty paragraph.


```js
ensureMinimum()
```

### Examples

Clears main text from all sections from the document leaving the sections themselves.

```js
let doc = new aw.Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.removeAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
let section = new aw.Section(doc);
doc.appendChild(section);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
let body = new aw.Body(doc);
section.appendChild(body);

// This body has no children, so we cannot add runs to it yet.
expect(doc.firstSection.body.getChildNodes(aw.NodeType.Any, true).count).toEqual(0);

// Call the "EnsureMinimum" to make sure that this body contains at least one empty paragraph. 
body.ensureMinimum();

// Now, we can add runs to the body, and get the document to display them.
body.firstParagraph.appendChild(new aw.Run(doc, "Hello world!"));

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [Body](../)

