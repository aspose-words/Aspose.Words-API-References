---
title: Font.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "Font.color property. Gets or sets the color of the font."
type: docs
weight: 70
url: /zh/python-net/aspose.words/font/color/
---

## Font.color property

Gets or sets the color of the font.


```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to insert formatted text using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 指定字体格式，然后添加文本。
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Courier New'
font.underline = aw.Underline.DASH
builder.write('Hello world!')
```

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

* module [aspose.words](../../)
* class [Font](../)

