---
title: TabStop.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "TabStop.position property. Gets the position of the tab stop in points."
type: docs
weight: 50
url: /ru/python-net/aspose.words/tabstop/position/
---

## TabStop.position property

Gets the position of the tab stop in points.


```python
@property
def position(self) -> float:
    ...

```

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(file_name=MY_DIR + 'Table of contents.docx')
# Итерируйте все абзацы со стилями, основанными на результатах TOC; это любой стиль от TOC до TOC9.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9:
        # Получите первую табуляцию, используемую в этом абзаце; она должна использоваться для выравнивания номеров страниц.
        tab = para.paragraph_format.tab_stops[0]
        # Замените первую табуляцию по умолчанию, остановку замените пользовательской табуляцией.
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(position=tab.position - 50, alignment=tab.alignment, leader=tab.leader)
doc.save(file_name=ARTIFACTS_DIR + 'Styles.ChangeTocsTabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStop](../)

