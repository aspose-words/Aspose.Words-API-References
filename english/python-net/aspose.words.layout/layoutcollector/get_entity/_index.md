---
title: get_entity method
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns an opaque position of the [LayoutEnumerator](../../layoutenumerator/) which corresponds to the specified node"
type: docs
weight: 50
url: /python-net/aspose.words.layout/layoutcollector/get_entity/
---

## get_entity(node) {#node}

Returns an opaque position of the [LayoutEnumerator](../../layoutenumerator/) which corresponds to the specified node.
You can use returned value as an argument to [LayoutEnumerator.current](../../layoutenumerator/current/) given the document being
enumerated and the document of the node are the same.



```python
def get_entity(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../../aspose.words/node/) |  |

This method works for only [Paragraph](../../../aspose.words/paragraph/) nodes, as well as indivisible inline nodes,
e.g. [BookmarkStart](../../../aspose.words/bookmarkstart/) or [Shape](../../../aspose.words.drawing/shape/). It doesn't work for [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) or [Table](../../../aspose.words.tables/table/) nodes, and nodes within header/footer.

Note that the entity returned for a [Paragraph](../../../aspose.words/paragraph/) node is a paragraph break span. Use the appropriate method to ascend to the parent line

If you need to navigate to a [Run](../../../aspose.words/run/) of text then you can insert bookmark right before it
and then navigate to the bookmark instead.

If you need to navigate to a [Cell](../../../aspose.words.tables/cell/) node then you can move to a [Paragraph](../../../aspose.words/paragraph/)
node in this cell and then ascend to a parent entity. The same approach can be used for [Row](../../../aspose.words.tables/row/)
and [Table](../../../aspose.words.tables/table/) nodes.




### Examples

Shows how to see the the ranges of pages that a node spans.

```python
doc = aw.Document()
layout_collector = aw.layout.LayoutCollector(doc)

# Call the "get_num_pages_spanned" method to count how many pages the content of our document spans.
# Since the document is empty, that number of pages is currently zero.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))

# Populate the document with 5 pages of content.
builder = aw.DocumentBuilder(doc)
builder.write("Section 1")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write("Section 2")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)

# Before the layout collector, we need to call the "update_page_layout" method to give us
# an accurate figure for any layout-related metric, such as the page count.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))

layout_collector.clear()
doc.update_page_layout()

self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))

# We can see the numbers of the start and end pages of any node and their overall page spans.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f"->  NodeType.{node.node_type}: ")
    print(
        f"\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)}," +
        f" spanning {layout_collector.get_num_pages_spanned(node)} pages.")

# We can iterate over the layout entities using a LayoutEnumerator.
layout_enumerator = aw.layout.LayoutEnumerator(doc)

self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)

# The LayoutEnumerator can traverse the collection of layout entities like a tree.
# We can also apply it to any node's corresponding layout entity.
layout_enumerator.current = layout_collector.get_entity(doc.get_child(aw.NodeType.PARAGRAPH, 1, True))

self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual("¶", layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

