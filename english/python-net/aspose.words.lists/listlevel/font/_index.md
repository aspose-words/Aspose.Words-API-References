---
title: ListLevel.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ListLevel.font property. Specifies character formatting used for the list label."
type: docs
weight: 30
url: /python-net/aspose.words.lists/listlevel/font/
---

## ListLevel.font property

Specifies character formatting used for the list label.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Create a list from a Microsoft Word template, and customize the first two of its list levels.
list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)

list_level = list.list_levels[0]
list_level.font.color = drawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = "\u0000"

list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144

list_level = list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = "Wingdings"
list_level.font.color = drawing.Color.blue
list_level.font.size = 24

# This NumberFormat value will create star-shaped bullet list symbols.
list_level.number_format = "\uf0af"
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144

# Create paragraphs and apply both list levels of our custom list formatting to them.
builder = aw.DocumentBuilder(doc)

builder.list_format.list = list
builder.writeln("The quick brown fox...")
builder.writeln("The quick brown fox...")

builder.list_format.list_indent()
builder.writeln("jumped over the lazy dog.")
builder.writeln("jumped over the lazy dog.")

builder.list_format.list_outdent()
builder.writeln("The quick brown fox...")

builder.list_format.remove_numbers()

builder.document.save(ARTIFACTS_DIR + "Lists.create_custom_list.docx")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

