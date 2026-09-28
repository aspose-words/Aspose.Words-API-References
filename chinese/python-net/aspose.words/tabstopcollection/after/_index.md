---
title: TabStopCollection.after method
linktitle: after method
articleTitle: after method
second_title: Aspose.Words for Python
description: "TabStopCollection.after method. Gets a first tab stop to the right of the specified position."
type: docs
weight: 40
url: /zh/python-net/aspose.words/tabstopcollection/after/
---

## after(position) {#float}

Gets a first tab stop to the right of the specified position.


```python
def after(self, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float | The reference position (in points). |

### Remarks

Skips tab stops with [TabStop.alignment](../../tabstop/alignment/) set to [TabAlignment.BAR](../../tabalignment/#BAR).




### Returns

A tab stop object or ``None`` if a suitable tab stop was not found.


### Examples

Shows how to work with a document's collection of tab stops.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
tab_stops = builder.paragraph_format.tab_stops
# 72 磅相当于 Microsoft Word 制表位尺上的"一英寸"。
tab_stops.add(tab_stop=aw.TabStop(position=72))
tab_stops.add(tab_stop=aw.TabStop(position=432, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.DASHES))
self.assertEqual(2, tab_stops.count)
self.assertFalse(tab_stops[0].is_clear)
self.assertFalse(tab_stops[0].equals(tab_stops[1]))
# 每个 "tab" 字符会将构建器的光标移动到下一个制表位的位置。
builder.writeln('Start\tTab 1\tTab 2')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(2, paragraphs.count)
# 每个段落都有其制表位集合，该集合从文档构建器的制表位集合克隆其值。
self.assertEqual(paragraphs[0].paragraph_format.tab_stops, paragraphs[1].paragraph_format.tab_stops)
# 制表位集合可以指向某些位置前后的 TabStops。
self.assertEqual(72, tab_stops.before(100).position)
self.assertEqual(432, tab_stops.after(100).position)
# 我们可以清除段落的制表位集合，以恢复默认的制表行为。
paragraphs[1].paragraph_format.tab_stops.clear()
self.assertEqual(0, paragraphs[1].paragraph_format.tab_stops.count)
doc.save(file_name=ARTIFACTS_DIR + 'TabStopCollection.TabStopCollection.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

