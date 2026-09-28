---
title: Font.underline property
linktitle: underline property
articleTitle: underline property
second_title: Aspose.Words for Python
description: "Font.underline property. Gets or sets the type of underline applied to the font."
type: docs
weight: 540
url: /zh/python-net/aspose.words/font/underline/
---

## Font.underline property

Gets or sets the type of underline applied to the font.


```python
@property
def underline(self) -> aspose.words.Underline:
    ...

@underline.setter
def underline(self, value: aspose.words.Underline):
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

Shows how to configure the style and color of a text underline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.underline = aw.Underline.DOTTED
builder.font.underline_color = aspose.pydrawing.Color.red
builder.writeln('Underlined text.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Underlines.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

