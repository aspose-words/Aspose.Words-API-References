---
title: LayoutCollector constructor
linktitle: LayoutCollector constructor
articleTitle: LayoutCollector constructor
second_title: Aspose.Words for Python
description: "LayoutCollector constructor. Initializes an instance of this class."
type: docs
weight: 10
url: /sv/python-net/aspose.words.layout/layoutcollector/__init__/
---

## LayoutCollector(doc) {#document}

Initializes an instance of this class.


```python
def __init__(self, doc: aspose.words.Document):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../../aspose.words/document/) | The document to which this collector instance will be attached to. |

### Examples

Shows how to see the the ranges of pages that a node spans.

```python
doc = aw.Document()
layout_collector = aw.layout.LayoutCollector(doc)
# Anropa metoden "GetNumPagesSpanned" för att räkna hur många sidor dokumentets innehåll sträcker sig över.
# Eftersom dokumentet är tomt är det antalet sidor för närvarande noll.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Fyll dokumentet med 5 sidor innehåll.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Innan layout‑samlaren måste vi anropa metoden "UpdatePageLayout" för att ge oss
# en exakt siffra för någon layoutrelaterad metrisk, såsom sidantalet.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Vi kan se siffrorna för start‑ och slut‑sidorna för vilken nod som helst och deras totala sidspann.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# Vi kan iterera över layout‑entiteterna med en LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# LayoutEnumerator kan traversera samlingen av layout‑entiteter som ett träd.
# Vi kan också applicera den på motsvarande layout‑entitet för vilken nod som helst.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

