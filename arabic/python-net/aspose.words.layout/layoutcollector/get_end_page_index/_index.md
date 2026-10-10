---
title: LayoutCollector.get_end_page_index method
linktitle: get_end_page_index method
articleTitle: get_end_page_index method
second_title: Aspose.Words for Python
description: "LayoutCollector.get_end_page_index method. Gets 1-based index of the page where node ends"
type: docs
weight: 40
url: /ar/python-net/aspose.words.layout/layoutcollector/get_end_page_index/
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
# استدعِ طريقة "GetNumPagesSpanned" لحساب عدد الصفحات التي يمتد محتوى مستندنا عبرها.
# نظرًا لأن المستند فارغ، فإن عدد الصفحات الحالي هو صفر.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# املأ المستند بـ 5 صفحات من المحتوى.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# قبل جامع التخطيط، نحتاج إلى استدعاء طريقة "UpdatePageLayout" لتزويدنا
# برقم دقيق لأي مقياس متعلق بالتخطيط، مثل عدد الصفحات.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# يمكننا رؤية أرقام الصفحات البداية والنهاية لأي عقدة ومدى الصفحات الإجمالي لها.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# يمكننا التكرار على كيانات التخطيط باستخدام LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# يمكن لـ LayoutEnumerator استعراض مجموعة كيانات التخطيط مثل شجرة.
# يمكننا أيضًا تطبيقه على كيان التخطيط المقابل لأي عقدة.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

