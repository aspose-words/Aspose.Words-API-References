---
title: LayoutCollector.get_start_page_index method
linktitle: get_start_page_index method
articleTitle: get_start_page_index method
second_title: Aspose.Words for Python
description: "LayoutCollector.get_start_page_index method. Gets 1-based index of the page where node begins"
type: docs
weight: 60
url: /ru/python-net/aspose.words.layout/layoutcollector/get_start_page_index/
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
# Вызовите метод "GetNumPagesSpanned", чтобы подсчитать, сколько страниц охватывает содержимое нашего документа.
# Поскольку документ пуст, количество страниц в данный момент равно нулю.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Заполните документ 5 страницами содержимого.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Перед сборщиком макета нам нужно вызвать метод "UpdatePageLayout", чтобы получить
# точную величину для любой метрики, связанной с макетом, например количество страниц.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Мы можем увидеть номера начальной и конечной страниц любого узла и их общие диапазоны страниц.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# Мы можем перебрать элементы макета, используя LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# LayoutEnumerator может обходить коллекцию элементов макета как дерево.
# Мы также можем применить его к соответствующему элементу макета любого узла.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

