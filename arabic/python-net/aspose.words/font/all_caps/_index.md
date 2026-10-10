---
title: Font.all_caps property
linktitle: all_caps property
articleTitle: all_caps property
second_title: Aspose.Words for Python
description: "Font.all_caps property. True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /ar/python-net/aspose.words/font/all_caps/
---

## Font.all_caps property

True if the font is formatted as all capital letters.


```python
@property
def all_caps(self) -> bool:
    ...

@all_caps.setter
def all_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# هناك طريقتان لجعل تشغيل يعرض نصه الصغير بالحروف الكبيرة دون تغيير المحتوى.
# 1 - اضبط علامة AllCaps لعرض جميع الأحرف بأحرف كبيرة عادية:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 - اضبط علامة SmallCaps لعرض جميع الأحرف بأحرف صغيرة:
# إذا كان الحرف صغيرًا، سيظهر بصورته الكبيرة
# لكن سيكون له نفس ارتفاع الحرف الصغير (ارتفاع x للخط).
# الأحرف التي كانت بحروف كبيرة أصلاً ستظهر كما هي.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

