---
title: TabStopCollection.remove_by_position method
linktitle: remove_by_position method
articleTitle: remove_by_position method
second_title: Aspose.Words for Python
description: "TabStopCollection.remove_by_position method. Removes a tab stop at the specified position from the collection."
type: docs
weight: 110
url: /ar/python-net/aspose.words/tabstopcollection/remove_by_position/
---

## remove_by_position(position) {#float}

Removes a tab stop at the specified position from the collection.


```python
def remove_by_position(self, position: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | float | The position (in points) of the tab stop to remove. |

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(file_name=MY_DIR + 'Table of contents.docx')
# تكرار عبر جميع الفقرات ذات الأنماط المستندة إلى نتيجة الفهرس؛ هذا أي نمط بين TOC و TOC9.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9:
        # احصل على أول علامة تبويب مستخدمة في هذه الفقرة، يجب أن تكون علامة التبويب المستخدمة لمحاذاة أرقام الصفحات.
        tab = para.paragraph_format.tab_stops[0]
        # استبدل أول علامة تبويب افتراضية، توقف باستخدام علامة تبويب مخصصة.
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(position=tab.position - 50, alignment=tab.alignment, leader=tab.leader)
doc.save(file_name=ARTIFACTS_DIR + 'Styles.ChangeTocsTabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [TabStopCollection](../)

