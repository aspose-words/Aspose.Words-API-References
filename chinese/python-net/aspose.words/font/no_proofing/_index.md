---
title: Font.no_proofing property
linktitle: no_proofing property
articleTitle: no_proofing property
second_title: Aspose.Words for Python
description: "Font.no_proofing property. True when the formatted characters are not to be spell checked."
type: docs
weight: 280
url: /zh/python-net/aspose.words/font/no_proofing/
---

## Font.no_proofing property

True when the formatted characters are not to be spell checked.


```python
@property
def no_proofing(self) -> bool:
    ...

@no_proofing.setter
def no_proofing(self, value: bool):
    ...

```

### Examples

Shows how to prevent text from being spell checked by Microsoft Word.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 通常，Microsoft Word 会使用锯齿形红色下划线突出显示拼写错误。
# 我们可以取消设置 "NoProofing" 标志，以创建一段文本，使其
# 绕过拼写检查器，同时完全禁用它。
builder.font.no_proofing = True
builder.writeln('Proofing has been disabled, so these spelking errrs will not display red lines underneath.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NoProofing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

