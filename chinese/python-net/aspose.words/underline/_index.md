---
title: Underline enumeration
linktitle: Underline enumeration
articleTitle: Underline enumeration
second_title: Aspose.Words for Python
description: "aspose.words.Underline enumeration. Indicates type of the underline applied to a font."
type: docs
weight: 1400
url: /zh/python-net/aspose.words/underline/
---

## Underline enumeration

Indicates type of the underline applied to a font.


### Members

| Name | Description |
| --- | --- |
| NONE |  |
| SINGLE |  |
| WORDS |  |
| DOUBLE |  |
| DOTTED |  |
| THICK |  |
| DASH |  |
| DASH_LONG |  |
| DOT_DASH |  |
| DOT_DOT_DASH |  |
| WAVY |  |
| DOTTED_HEAVY |  |
| DASH_HEAVY |  |
| DASH_LONG_HEAVY |  |
| DOT_DASH_HEAVY |  |
| DOT_DOT_DASH_HEAVY |  |
| WAVY_HEAVY |  |
| WAVY_DOUBLE |  |

### Examples

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('For more information, please visit the ')
# 插入超链接并使用自定义格式进行强调。
# 该超链接将是可点击的文本，点击后会跳转到 URL 中指定的位置。
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# 在 Microsoft Word 中按 Ctrl 并左键单击文本中的链接，会通过新浏览器窗口打开该 URL。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

### See Also

* module [aspose.words](../)

