---
title: Font.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "Font.color property. Gets or sets the color of the font."
type: docs
weight: 70
url: /python-net/aspose.words/font/color/
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
builder = aw.DocumentBuilder(doc)

# Specify font formatting, then add text.
font = builder.font
font.size = 16
font.bold = True
font.color = drawing.Color.blue
font.name = "Courier New"
font.underline = aw.Underline.DASH

builder.write("Hello world!")
```

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("For more information, please visit the ")

# Insert a hyperlink and emphasize it with custom formatting.
# The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = drawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink("Google website", "https://www.google.com", False)
builder.font.clear_formatting()
builder.writeln(".")

# Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_hyperlink.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

