---
title: list_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to the list formatting properties of a paragraph style."
type: docs
weight: 110
url: /python-net/aspose.words/style/list_format/
---

## Style.list_format property

Provides access to the list formatting properties of a paragraph style.

This property is only valid for paragraph styles.
For other style types this property returns ``None``.




### Examples

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

