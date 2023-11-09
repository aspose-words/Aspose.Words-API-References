---
title: Style.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "Style.font property. Gets the character formatting of the style."
type: docs
weight: 60
url: /python-net/aspose.words/style/font/
---

## Style.font property

Gets the character formatting of the style.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

For list styles this property returns ``None``.




### Examples

Shows how to create and apply a custom style.

```python
doc = aw.Document()

style = doc.styles.add(aw.StyleType.PARAGRAPH, "MyStyle")
style.font.name = "Times New Roman"
style.font.size = 16
style.font.color = drawing.Color.navy
# Automatically redefine style.
style.automatically_update = True

builder = aw.DocumentBuilder(doc)

# Apply one of the styles from the document to the paragraph that the document builder is creating.
builder.paragraph_format.style = doc.styles.get_by_name("MyStyle")
builder.writeln("Hello world!")

first_paragraph_style = doc.first_section.body.first_paragraph.paragraph_format.style

self.assertEqual(style, first_paragraph_style)

# Remove our custom style from the document's styles collection.
doc.styles.get_by_name("MyStyle").remove()

first_paragraph_style = doc.first_section.body.first_paragraph.paragraph_format.style

# Any text that used a removed style reverts to the default formatting.
self.assertFalse(any(s.name == "MyStyle" for s in doc.styles))
self.assertEqual("Times New Roman", first_paragraph_style.font.name)
self.assertEqual(12.0, first_paragraph_style.font.size)
self.assertEqual(drawing.Color.empty().to_argb(), first_paragraph_style.font.color.to_argb())
```

Shows how to create and use a paragraph style with list formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a custom paragraph style.
style = doc.styles.add(aw.StyleType.PARAGRAPH, "MyStyle1")
style.font.size = 24
style.font.name = "Verdana"
style.paragraph_format.space_after = 12

# Create a list and make sure the paragraphs that use this style will use this list.
style.list_format.list = doc.lists.add(aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0

# Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.paragraph_format.style = style
builder.writeln("Hello World: MyStyle1, bulleted list.")

# Change the document builder's style to one that has no list formatting and write another paragraph.
builder.paragraph_format.style = doc.styles.get_by_name("Normal")
builder.writeln("Hello World: Normal.")

builder.document.save(ARTIFACTS_DIR + "Styles.paragraph_style_bulleted_list.docx")
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

