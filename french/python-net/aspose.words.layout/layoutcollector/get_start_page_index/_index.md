---
title: LayoutCollector.get_start_page_index method
linktitle: get_start_page_index method
articleTitle: get_start_page_index method
second_title: Aspose.Words for Python
description: "LayoutCollector.get_start_page_index method. Gets 1-based index of the page where node begins"
type: docs
weight: 60
url: /fr/python-net/aspose.words.layout/layoutcollector/get_start_page_index/
---

## get_start_page_index(node) {#node}

Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page.


```python
def get_start_page_index(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../../aspose.words/node/) |  |

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

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

