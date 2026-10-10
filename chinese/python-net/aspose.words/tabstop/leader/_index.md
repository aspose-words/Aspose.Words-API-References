---
title: TabStop.leader property
linktitle: leader property
articleTitle: leader property
second_title: Aspose.Words for Python
description: "TabStop.leader property. Gets or sets the type of the leader line displayed under the tab character."
type: docs
weight: 40
url: /zh/python-net/aspose.words/tabstop/leader/
---

## TabStop.leader property

Gets or sets the type of the leader line displayed under the tab character.


```python
@property
def leader(self) -> aspose.words.TabLeader:
    ...

@leader.setter
def leader(self, value: aspose.words.TabLeader):
    ...

```

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(file_name=MY_DIR + 'Table of contents.docx')
# 遍历所有使用 TOC 结果样式的段落；这指的是介于 TOC 和 TOC9 之间的任何样式。
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9:
        # 获取此段落中使用的第一个制表符，这应该是用于对齐页码的制表符。
        tab = para.paragraph_format.tab_stops[0]
        # 用自定义制表位替换第一个默认制表符。
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(position=tab.position - 50, alignment=tab.alignment, leader=tab.leader)
doc.save(file_name=ARTIFACTS_DIR + 'Styles.ChangeTocsTabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStop](../)

