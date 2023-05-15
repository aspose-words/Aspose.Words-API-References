﻿---
title: Style class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a single built-in or user-defined style"
type: docs
weight: 1100
url: /python-net/aspose.words/style/
---

## Style class

Represents a single built-in or user-defined style.
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/python-net/working-with-styles-and-themes/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [aliases](./aliases/) | Gets all aliases of this style. If style has no aliases then empty array of string is returned. |
| [automatically_update](./automatically_update/) | Specifies whether this style is automatically redefined based on the appropriate value. |
| [base_style_name](./base_style_name/) | Gets/sets the name of the style this style is based on. |
| [built_in](./built_in/) | True if this style is one of the built-in styles in MS Word. |
| [document](./document/) | Gets the owner document. |
| [font](./font/) | Gets the character formatting of the style. |
| [is_heading](./is_heading/) | True when the style is one of the built-in Heading styles. |
| [is_quick_style](./is_quick_style/) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [linked_style_name](./linked_style_name/) | Gets the name of the [Style](./) linked to this one. Returns empty string if no styles are linked. |
| [list](./list/) | Gets the list that defines formatting of this list style. |
| [list_format](./list_format/) | Provides access to the list formatting properties of a paragraph style. |
| [name](./name/) | Gets or sets the name of the style. |
| [next_paragraph_style_name](./next_paragraph_style_name/) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [paragraph_format](./paragraph_format/) | Gets the paragraph formatting of the style. |
| [style_identifier](./style_identifier/) | Gets the locale independent style identifier for a built-in style. |
| [styles](./styles/) | Gets the collection of styles this style belongs to. |
| [type](./type/) | Gets the style type (paragraph or character). |

### Methods

| Name | Description |
| --- | --- |
|[ as_table_style()](./as_table_style/#default) |  |
|[ equals(style)](./equals/#style) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared. |
|[ remove()](./remove/#default) | Removes the specified style from the document. |

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

* module [aspose.words](../)

