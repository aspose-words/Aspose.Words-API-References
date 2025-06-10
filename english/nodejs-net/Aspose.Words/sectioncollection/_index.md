---
title: SectionCollection class
linktitle: SectionCollection class
articleTitle: SectionCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.SectionCollection class. A collection of [Section](../section/) objects in the document"
type: docs
weight: 1150
url: /nodejs-net/aspose.words/sectioncollection/
---

## SectionCollection class

A collection of [Section](../section/) objects in the document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/nodejs-net/working-with-sections/) documentation article.




### Remarks

A Microsoft Word document can contain multiple sections. To create a section in a Microsoft Word,
select the Insert/Break command and select a break type. The break specifies whether section starts
on a new page or on the same page.

Programmatically inserting and removing sections can be used to customize documents produced
during mail merge. If a document needs to have different content or parts of the
content depending on some criteria, then you can create a "master" document that contains
multiple sections and delete some of the sections before or after mail merge.




**Inheritance:** [SectionCollection](./) → [NodeCollection](../nodecollection/)

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
| [this[]](../nodecollection/this[]/) | <br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ indexOf(node)](../nodecollection/indexOf/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#number_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ removeAt(index)](../nodecollection/removeAt/#number) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ toArray()](./toArray/#default) | Copies all sections from the collection to a new array of sections. |

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

* module [Aspose.Words](../)
* class [NodeCollection](../nodecollection/)

