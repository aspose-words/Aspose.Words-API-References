---
title: LayoutCollector.get_end_page_index method
linktitle: get_end_page_index method
articleTitle: get_end_page_index method
second_title: Aspose.Words for Python
description: "LayoutCollector.get_end_page_index method. Gets 1-based index of the page where node ends"
type: docs
weight: 40
url: /it/python-net/aspose.words.layout/layoutcollector/get_end_page_index/
---

## get_end_page_index(node) {#node}

Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page.


```python
def get_end_page_index(self, node: aspose.words.Node):
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
# Chiama il metodo "GetNumPagesSpanned" per contare quante pagine occupa il contenuto del nostro documento.
# Poiché il documento è vuoto, quel numero di pagine è attualmente zero.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Popola il documento con 5 pagine di contenuto.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Prima del raccoglitore di layout, dobbiamo chiamare il metodo "UpdatePageLayout" per fornirci
# una misura accurata per qualsiasi metrica legata al layout, come il conteggio delle pagine.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Possiamo vedere i numeri delle pagine di inizio e fine di qualsiasi nodo e la loro estensione complessiva.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# Possiamo iterare sulle entità di layout usando un LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# Il LayoutEnumerator può attraversare la collezione di entità di layout come un albero.
# Possiamo anche applicarlo all'entità di layout corrispondente di qualsiasi nodo.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

