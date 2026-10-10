---
title: Paragraph.get_effective_tab_stops method
linktitle: get_effective_tab_stops method
articleTitle: get_effective_tab_stops method
second_title: Aspose.Words for Python
description: "Paragraph.get_effective_tab_stops method. Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists."
type: docs
weight: 270
url: /zh/python-net/aspose.words/paragraph/get_effective_tab_stops/
---

## get_effective_tab_stops() {#default}

Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists.


```python
def get_effective_tab_stops(self):
    ...
```

### Examples

Shows how to set custom tab stops for a paragraph.

```python
doc = aw.Document()
para = doc.first_section.body.first_paragraph
# 如果我们位于此集合中没有制表位的段落，
# 每次在 Microsoft Word 中按 Tab 键，光标将跳动 36 磅。
self.assertEqual(0, len(doc.first_section.body.first_paragraph.get_effective_tab_stops()))
# 如果通过 \"View\" 选项卡启用标尺，我们可以在 Microsoft Word 中添加自定义制表位。
# 此标尺上的每个单位相当于两个默认制表位，即 72 磅。
# 我们可以像这样以编程方式添加自定义制表位。
tab_stops = doc.first_section.body.first_paragraph.paragraph_format.tab_stops
tab_stops.add(position=72, alignment=aw.TabAlignment.LEFT, leader=aw.TabLeader.DOTS)
tab_stops.add(position=216, alignment=aw.TabAlignment.CENTER, leader=aw.TabLeader.DASHES)
tab_stops.add(position=360, alignment=aw.TabAlignment.RIGHT, leader=aw.TabLeader.LINE)
# 通过 \"View\" -> \"Show\" -> \"Ruler\" 启用标尺后，我们可以在 Microsoft Word 中看到这些制表位。
self.assertEqual(3, len(para.get_effective_tab_stops()))
# 我们添加的任何制表符都会使用标尺上的制表位，并且可能，
# 根据制表前导符的值，在制表起点和终点之间留下空格。
para.append_child(aw.Run(doc=doc, text='\tTab 1\tTab 2\tTab 3'))
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.TabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

