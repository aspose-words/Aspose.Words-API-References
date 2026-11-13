---
title: LayoutCollector.get_num_pages_spanned method
linktitle: get_num_pages_spanned method
articleTitle: get_num_pages_spanned method
second_title: Aspose.Words for Python
description: "LayoutCollector.get_num_pages_spanned method. Gets number of pages the specified node spans"
type: docs
weight: 50
url: /es/python-net/aspose.words.layout/layoutcollector/get_num_pages_spanned/
---

## get_num_pages_spanned(node) {#node}

Gets number of pages the specified node spans. 0 if node is within a single page.
This is the same as [LayoutCollector.get_end_page_index()](../get_end_page_index/#node) - [LayoutCollector.get_start_page_index()](../get_start_page_index/#node).



```python
def get_num_pages_spanned(self, node: aspose.words.Node):
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
# Llame al método "GetNumPagesSpanned" para contar cuántas páginas abarca el contenido de nuestro documento.
# Dado que el documento está vacío, ese número de páginas es actualmente cero.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Rellene el documento con 5 páginas de contenido.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Antes del recopilador de diseño, necesitamos llamar al método "UpdatePageLayout" para darnos
# una cifra precisa para cualquier métrica relacionada con el diseño, como el recuento de páginas.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Podemos ver los números de las páginas de inicio y fin de cualquier nodo y sus extensiones de página totales.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# Podemos iterar sobre las entidades de diseño usando un LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# El LayoutEnumerator puede recorrer la colección de entidades de diseño como un árbol.
# También podemos aplicarlo a la entidad de diseño correspondiente a cualquier nodo.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

