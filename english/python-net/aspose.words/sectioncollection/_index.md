---
title: SectionCollection class
linktitle: SectionCollection class
articleTitle: SectionCollection class
second_title: Aspose.Words for Python
description: "aspose.words.SectionCollection class. A collection of [Section](../section/) objects in the document"
type: docs
weight: 970
url: /python-net/aspose.words/sectioncollection/
---

## SectionCollection class

A collection of [Section](../section/) objects in the document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/python-net/working-with-sections/) documentation article.




### Remarks

A Microsoft Word document can contain multiple sections. To create a section in a Microsoft Word,
select the Insert/Break command and select a break type. The break specifies whether section starts
on a new page or on the same page.

Programmatically inserting and removing sections can be used to customize documents produced
during mail merge. If a document needs to have different content or parts of the
content depending on some criteria, then you can create a "master" document that contains
multiple sections and delete some of the sections before or after mail merge.




**Inheritance:** [SectionCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a section at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all sections from the collection to a new array of sections. |

### Examples

Shows how to add and remove sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
self.assertEqual('Section 1\x0cSection 2', doc.get_text().strip())
# Delete the first section from the document.
doc.sections.remove_at(0)
self.assertEqual('Section 2', doc.get_text().strip())
# Append a copy of what is now the first section to the end of the document.
last_section_idx = doc.sections.count - 1
new_section = doc.sections[last_section_idx].clone()
doc.sections.add(new_section)
self.assertEqual('Section 2\x0cSection 2', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

