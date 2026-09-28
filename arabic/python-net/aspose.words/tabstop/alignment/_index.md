---
title: TabStop.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "TabStop.alignment property. Gets or sets the alignment of text at this tab stop."
type: docs
weight: 20
url: /ar/python-net/aspose.words/tabstop/alignment/
---

## TabStop.alignment property

Gets or sets the alignment of text at this tab stop.


```python
@property
def alignment(self) -> aspose.words.TabAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.TabAlignment):
    ...

```

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
* class [TabStop](../)

