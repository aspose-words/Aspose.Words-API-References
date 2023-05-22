---
title: ListFormat.list property
linktitle: list property
articleTitle: list property
second_title: Aspose.Words for Python
description: "ListFormat.list property. Gets or sets the list this paragraph is a member of."
type: docs
weight: 20
url: /python-net/aspose.words.lists/listformat/list/
---

## ListFormat.list property

Gets or sets the list this paragraph is a member of.

The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to ``None`` removes bullets and numbering from the paragraph
and sets the list level number to zero. Setting this property to ``None`` is equivalent
to calling [ListFormat.remove_numbers()](../remove_numbers/#default).




### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

self.assertFalse(builder.list_format.is_list_item)

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Below are two types of lists that we can create using a document builder.
# 1 -  A numbered list:
# Numbered lists create a logical order for their paragraphs by numbering each item.
builder.list_format.list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)

self.assertTrue(builder.list_format.is_list_item)

# By setting the "list_level_number" property, we can increase the list level
# to begin a self-contained sub-list at the current list item.
# The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
# Deeper list levels use letters and lowercase Roman numerals.
for i in range(9):

    builder.list_format.list_level_number = i
    builder.writeln(f"Level {i}")

# 2 -  A bulleted list:
# This list will apply an indent and a bullet symbol ("•") before each paragraph.
# Deeper levels of this list will use different symbols, such as "■" and "○".
builder.list_format.list = doc.lists.add(aw.lists.ListTemplate.BULLET_DEFAULT)

for i in range(9):
    builder.list_format.list_level_number = i
    builder.writeln(f"Level {i}")

# We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.list_format.list = None

self.assertFalse(builder.list_format.is_list_item)

doc.save(ARTIFACTS_DIR + "Lists.specify_list_level.docx")
```

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Create an outline list for the headings.
outline_list = doc.lists.add(aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln("This is my Chapter 1")

# Create a numbered list.
numbered_list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln("Numbered list item 1.")

# Every paragraph that comprises a list will have this flag.
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)

# Create a bulleted list.
bulleted_list = doc.lists.add(aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln("Bulleted list item 1.")
builder.writeln("Bulleted list item 2.")
builder.paragraph_format.clear_formatting()

# Revert to the numbered list.
builder.list_format.list = numbered_list
builder.writeln("Numbered list item 2.")
builder.writeln("Numbered list item 3.")

# Revert to the outline list.
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln("This is my Chapter 2")

builder.paragraph_format.clear_formatting()

builder.document.save(ARTIFACTS_DIR + "Lists.nested_lists.docx")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list_level_number](../list_level_number/)
* method [ListFormat.remove_numbers()](../remove_numbers/#default)

