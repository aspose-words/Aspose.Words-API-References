---
title: LayoutCollector class
linktitle: LayoutCollector class
articleTitle: LayoutCollector class
second_title: Aspose.Words for Python
description: "aspose.words.layout.LayoutCollector class. This class allows to compute page numbers of document nodes."
type: docs
weight: 40
url: /fr/python-net/aspose.words.layout/layoutcollector/
---

## LayoutCollector class

This class allows to compute page numbers of document nodes.

To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/python-net/converting-to-fixed-page-format/) documentation article.




### Remarks

When you create a [LayoutCollector](./) and specify a [Document](../../aspose.words/document/) document object to attach to, 
the collector will record mapping of document nodes to layout objects when the document is formatted into pages.

You will be able to find out on which page a particular document node (e.g. run, paragraph or table cell) is located
by using the [LayoutCollector.get_start_page_index()](./get_start_page_index/#node), [LayoutCollector.get_end_page_index()](./get_end_page_index/#node) and [LayoutCollector.get_num_pages_spanned()](./get_num_pages_spanned/#node) methods. 
These methods automatically build page layout model of the document and update fields if required.

When you no longer need to collect layout information, it is best to set the [LayoutCollector.document](./document/) property to ``None``
to avoid unnecessary collection of more layout mappings.




### Constructors
| Name | Description |
| --- | --- |
| [LayoutCollector(doc)](./__init__/#document) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets or sets the document this collector instance is attached to. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt. |
|[ get_end_page_index(node)](./get_end_page_index/#node) | Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page. |
|[ get_num_pages_spanned(node)](./get_num_pages_spanned/#node) | Gets number of pages the specified node spans. 0 if node is within a single page. This is the same as [LayoutCollector.get_end_page_index()](./get_end_page_index/#node) - [LayoutCollector.get_start_page_index()](./get_start_page_index/#node). |
|[ get_start_page_index(node)](./get_start_page_index/#node) | Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page. |

### Examples

Shows how to see the the ranges of pages that a node spans.

```python
doc = aw.Document()
layout_collector = aw.layout.LayoutCollector(doc)
# Appelez la méthode "GetNumPagesSpanned" pour compter le nombre de pages que le contenu de notre document occupe.
# Comme le document est vide, ce nombre de pages est actuellement zéro.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Remplissez le document avec 5 pages de contenu.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Avant le collecteur de mise en page, nous devons appeler la méthode "UpdatePageLayout" pour nous fournir
# une mesure précise pour toute métrique liée à la mise en page, comme le nombre de pages.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Nous pouvons voir les numéros des pages de début et de fin de n'importe quel nœud ainsi que leurs étendues de pages globales.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# Nous pouvons itérer sur les entités de mise en page en utilisant un LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# Le LayoutEnumerator peut parcourir la collection d'entités de mise en page comme un arbre.
# Nous pouvons également l'appliquer à l'entité de mise en page correspondante de n'importe quel nœud.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../)

