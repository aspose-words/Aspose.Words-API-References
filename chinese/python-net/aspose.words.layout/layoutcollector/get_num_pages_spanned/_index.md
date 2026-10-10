---
title: LayoutCollector.get_num_pages_spanned method
linktitle: get_num_pages_spanned method
articleTitle: get_num_pages_spanned method
second_title: Aspose.Words for Python
description: "LayoutCollector.get_num_pages_spanned method. Gets number of pages the specified node spans"
type: docs
weight: 50
url: /zh/python-net/aspose.words.layout/layoutcollector/get_num_pages_spanned/
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
# 调用 "GetNumPagesSpanned" 方法来统计文档内容跨越了多少页。
# 由于文档为空，该页数目前为零。
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# 向文档填充 5 页内容。
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 在布局收集器之前，我们需要调用 "UpdatePageLayout" 方法来为我们提供
# 任何布局相关度量（例如页数）的准确数值。
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# 我们可以看到任意节点的起始页和结束页编号以及它们的整体跨页范围。
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# 我们可以使用 LayoutEnumerator 迭代布局实体。
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# LayoutEnumerator 可以像遍历树一样遍历布局实体集合。
# 我们也可以将其应用于任意节点对应的布局实体。
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

