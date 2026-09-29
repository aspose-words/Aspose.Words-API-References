---
title: Font.all_caps property
linktitle: all_caps property
articleTitle: all_caps property
second_title: Aspose.Words for Python
description: "Font.all_caps property. True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /ru/python-net/aspose.words/font/all_caps/
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
# Есть два способа заставить фрагмент отображать свой текст в нижнем регистре в верхнем регистре без изменения содержимого.
# 1 -  Установите флаг AllCaps, чтобы отображать все символы обычными заглавными буквами:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Установите флаг SmallCaps, чтобы отображать все символы в малых заглавных буквах:
# Если символ в нижнем регистре, он будет отображаться в своей верхней форме
# но будет иметь ту же высоту, что и нижний регистр (x-height шрифта).
# Символы, изначально находившиеся в верхнем регистре, будут выглядеть одинаково.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

