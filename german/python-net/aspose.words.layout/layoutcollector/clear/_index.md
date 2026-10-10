---
title: LayoutCollector.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "LayoutCollector.clear method. Clears all collected layout data"
type: docs
weight: 30
url: /de/python-net/aspose.words.layout/layoutcollector/clear/
---

## clear() {#default}

Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt.


```python
def clear(self):
    ...
```

### Examples

Shows how to see the the ranges of pages that a node spans.

```python
doc = aw.Document()
layout_collector = aw.layout.LayoutCollector(doc)
# Rufen Sie die "GetNumPagesSpanned"-Methode auf, um zu zählen, wie viele Seiten der Inhalt unseres Dokuments umfasst.
# Da das Dokument leer ist, beträgt die aktuelle Seitenzahl null.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Füllen Sie das Dokument mit 5 Seiten Inhalt.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Vor dem Layout-Collector müssen wir die "UpdatePageLayout"-Methode aufrufen, um uns
# eine genaue Angabe für jede layoutbezogene Kennzahl zu liefern, wie z. B. die Seitenanzahl.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Wir können die Nummern der Start- und Endseiten jedes Knotens sowie deren gesamte Seitenbereiche sehen.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# Wir können über die Layout-Entitäten mit einem LayoutEnumerator iterieren.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# Der LayoutEnumerator kann die Sammlung von Layout-Entitäten wie einen Baum durchlaufen.
# Wir können ihn auch auf die entsprechende Layout-Entität eines beliebigen Knotens anwenden.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

