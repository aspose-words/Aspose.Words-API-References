---
title: Font.underline property
linktitle: underline property
articleTitle: underline property
second_title: Aspose.Words for Python
description: "Font.underline property. Gets or sets the type of underline applied to the font."
type: docs
weight: 530
url: /python-net/aspose.words/font/underline/
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

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('For more information, please visit the ')
# Insert a hyperlink and emphasize it with custom formatting.
# The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

Shows how to insert formatted text using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Specify font formatting, then add text.
font = builder.font
font.size = 16
font.bold = True
font.color = aspose.pydrawing.Color.blue
font.name = 'Courier New'
font.underline = aw.Underline.DASH
builder.write('Hello world!')
```

Shows how to configure the style and color of a text underline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.underline = aw.Underline.DOTTED
builder.font.underline_color = aspose.pydrawing.Color.red
builder.writeln('Underlined text.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Underlines.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

