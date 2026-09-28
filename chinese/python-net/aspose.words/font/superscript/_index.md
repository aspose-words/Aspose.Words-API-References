---
title: Font.superscript property
linktitle: superscript property
articleTitle: superscript property
second_title: Aspose.Words for Python
description: "Font.superscript property. True if the font is formatted as superscript."
type: docs
weight: 450
url: /zh/python-net/aspose.words/font/superscript/
---

## Font.superscript property

True if the font is formatted as superscript.


```python
@property
def superscript(self) -> bool:
    ...

@superscript.setter
def superscript(self, value: bool):
    ...

```

### Examples

Shows how to format text to offset its position.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# 将此文本运行提升 5 磅高于基线。
run = aw.Run(doc=doc, text='Raised text. ')
run.font.position = 5
para.append_child(run)
# 将此文本运行降低 10 磅低于基线。
run = aw.Run(doc=doc, text='Lowered text. ')
run.font.position = -10
para.append_child(run)
# 添加一段普通文本。
run = aw.Run(doc=doc, text='Text in its default position. ')
para.append_child(run)
# 添加一段以下标形式显示的文本。
run = aw.Run(doc=doc, text='Subscript. ')
run.font.subscript = True
para.append_child(run)
# 添加一段以上标形式显示的文本。
run = aw.Run(doc=doc, text='Superscript.')
run.font.superscript = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.PositionSubscript.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

