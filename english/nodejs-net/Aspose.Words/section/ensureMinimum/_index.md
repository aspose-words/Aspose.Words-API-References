---
title: Section.ensureMinimum method
linktitle: ensureMinimum method
articleTitle: ensureMinimum method
second_title: Aspose.Words for NodeJs
description: "Section.ensureMinimum method. Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/)."
type: docs
weight: 130
url: /nodejs-net/aspose.words/section/ensureMinimum/
---

## ensureMinimum() {#default}

Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/).



```js
ensureMinimum()
```

### Examples

Shows how to prepare a new section node for editing.

```js
let doc = new aw.Document();

// A blank document comes with a section, which has a body, which in turn has a paragraph.
// We can add contents to this document by adding elements such as text runs, shapes, or tables to that paragraph.
expect(doc.getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Section);
expect(doc.sections.at(0).getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Body);
expect(doc.sections.at(0).body.getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Paragraph);

// If we add a new section like this, it will not have a body, or any other child nodes.
doc.sections.add(new aw.Section(doc));

expect(doc.sections.at(1).getChildNodes(aw.NodeType.Any, true).count).toEqual(0);

// Run the "EnsureMinimum" method to add a body and a paragraph to this section to begin editing it.
doc.lastSection.ensureMinimum();

expect(doc.sections.at(1).getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Body);
expect(doc.sections.at(1).body.getChild(aw.NodeType.Any, 0, true).nodeType).toEqual(aw.NodeType.Paragraph);

doc.sections.at(0).body.firstParagraph.appendChild(new aw.Run(doc, "Hello world!"));

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../../)
* class [Section](../)

