---
title: HeaderFooterCollection class
linktitle: HeaderFooterCollection class
articleTitle: HeaderFooterCollection class
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection class. Provides typed access to [HeaderFooter](../headerfooter/) nodes of a [Section](../section/)"
type: docs
weight: 490
url: /de/python-net/aspose.words/headerfootercollection/
---

## HeaderFooterCollection class

Provides typed access to [HeaderFooter](../headerfooter/) nodes of a [Section](../section/).
To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/python-net/working-with-headers-and-footers/) documentation article.




### Remarks

There can be maximum of one [HeaderFooter](../headerfooter/)


 of each[HeaderFooterType](../headerfootertype/) per
[Section](../section/).
[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.




**Inheritance:** [HeaderFooterCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [HeaderFooter](../headerfooter/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
| [footer_even](./footer_even/) | Retrieves a footer for even numbered pages. |
| [footer_first](./footer_first/) | Retrieves a footer for the first page of the section. |
| [footer_primary](./footer_primary/) | Retrieves a primary footer, also used for odd numbered pages. |
| [header_even](./header_even/) | Retrieves a header for even numbered pages. |
| [header_first](./header_first/) | Retrieves a header for the first page of the section. |
| [header_primary](./header_primary/) | Retrieves a primary header, also used for odd numbered pages. |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ get_by_header_footer_type(header_footer_type)](./get_by_header_footer_type/#headerfootertype) | Retrieves a **HeaderFooter** of the specified type. |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ link_to_previous(is_link_to_previous)](./link_to_previous/#bool) | Links or unlinks all headers and footers to the corresponding headers and footers in the previous section. |
|[ link_to_previous(header_footer_type, is_link_to_previous)](./link_to_previous/#headerfootertype_bool) | Links or unlinks the specified header or footer to the corresponding header or footer in the previous section. |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all ``HeaderFooter`` s from the collection to a new array of ``HeaderFooter`` s. |

### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()
# Erstellen Sie eine Kopfzeile und fügen Sie ihr einen Absatz hinzu. Der Text in diesem Absatz
# wird oben auf jeder Seite dieses Abschnitts erscheinen, über dem Haupttext.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# Erstellen Sie eine Fußzeile und fügen Sie ihr einen Absatz hinzu. Der Text in diesem Absatz
# wird unten auf jeder Seite dieses Abschnitts erscheinen, unter dem Haupttext.
footer = aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY)
doc.first_section.headers_footers.add(footer)
para = footer.append_paragraph('My footer.')
self.assertFalse(footer.is_header)
self.assertTrue(para.is_end_of_header_footer)
self.assertEqual(footer, para.parent_story)
self.assertEqual(footer.parent_section, para.parent_section)
self.assertEqual(footer.parent_section, header.parent_section)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Create.docx')
```

Shows how to delete all footers from a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# Iterieren Sie durch jeden Abschnitt und entfernen Sie Fußzeilen aller Art.
for section in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_section(), b), list(doc))):
    # Es gibt drei Arten von Fuß- und Kopfzeilentypen.
    # 1 -  Die "Erste" Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    footer = section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_FIRST)
    cond_expression = footer
    if cond_expression != None:
        cond_expression.remove()
    # 2 -  Die "Primäre" Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
    cond_expression2 = footer
    if cond_expression2 != None:
        cond_expression2.remove()
    # 3 -  Die "Gerade" Kopf-/Fußzeile, die auf geraden Seiten erscheint.
    footer = section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_EVEN)
    cond_expression3 = footer
    if cond_expression3 != None:
        cond_expression3.remove()
    self.assertEqual(0, len(list(filter(lambda hf: not hf.as_header_footer().is_header, section.headers_footers))))
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.RemoveFooters.docx')
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

