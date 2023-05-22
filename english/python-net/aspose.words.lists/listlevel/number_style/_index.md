---
title: ListLevel.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "ListLevel.number_style property. Returns or sets the number style for this list level."
type: docs
weight: 90
url: /python-net/aspose.words.lists/listlevel/number_style/
---

## ListLevel.number_style property

Returns or sets the number style for this list level.


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

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)

# Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
# These will look like "Appendix A", "Appendix B"...
list.list_levels[0].number_format = "Appendix \u0000"
list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
list.list_levels[0].linked_style = doc.styles.get_by_name("Heading 1")

# Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
# If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
list.list_levels[1].number_format = "Section (\u0000.\u0001)"
list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO

# Note that the higher-level uses UppercaseLetter numbering.
# We can set the "is_legal" property to use Arabic numbers for the higher list levels.
list.list_levels[1].is_legal = True
list.list_levels[1].restart_after_level = 0

# Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
# These list labels will look like "-I-", "-II-"...
list.list_levels[2].number_format = "-\u0002-"
list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
list.list_levels[2].restart_after_level = 1

# Make labels of all list levels bold.
for level in list.list_levels:
    level.font.bold = True

# Apply list formatting to the current paragraph.
builder.list_format.list = list

# Create list items that will display all three of our list levels.
for n in range(2):
    for i in range(3):
        builder.list_format.list_level_number = i
        builder.writeln(f"Level {i}")

builder.list_format.remove_numbers()

doc.save(ARTIFACTS_DIR + "Lists.create_list_restart_after_higher.docx")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

