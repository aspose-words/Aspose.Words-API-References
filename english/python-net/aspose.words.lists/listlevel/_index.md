---
title: ListLevel class
linktitle: ListLevel class
articleTitle: ListLevel class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListLevel class. Defines formatting for a list level"
type: docs
weight: 50
url: /python-net/aspose.words.lists/listlevel/
---

## ListLevel class

Defines formatting for a list level.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

You do not create objects of this class. List level objects are created automatically
when a list is created. You access [ListLevel](./) objects via the
[ListLevelCollection](../listlevelcollection/) collection.

Use the properties of [ListLevel](./) to specify list formatting
for individual list levels.




### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets the justification of the actual number of the list item. |
| [custom_number_style_format](./custom_number_style_format/) | Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...". |
| [font](./font/) | Specifies character formatting used for the list label. |
| [image_data](./image_data/) | Returns image data of the picture bullet shape for the current list level. |
| [is_legal](./is_legal/) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [linked_style](./linked_style/) | Gets or sets the paragraph style that is linked to this list level. |
| [number_format](./number_format/) | Returns or sets the number format for the list level. |
| [number_position](./number_position/) | Returns or sets the position (in points) of the number or bullet for the list level. |
| [number_style](./number_style/) | Returns or sets the number style for this list level. |
| [restart_after_level](./restart_after_level/) | Sets or returns the list level that must appear before the specified list level restarts numbering. |
| [start_at](./start_at/) | Returns or sets the starting number for this list level. |
| [tab_position](./tab_position/) | Returns or sets the tab position (in points) for the list level. |
| [text_position](./text_position/) | Returns or sets the position (in points) for the second line of wrapping text for the list level. |
| [trailing_character](./trailing_character/) | Returns or sets the character inserted after the number for the list level. |

### Methods

| Name | Description |
| --- | --- |
|[ create_picture_bullet()](./create_picture_bullet/#default) | Creates picture bullet shape for the current list level. |
|[ delete_picture_bullet()](./delete_picture_bullet/#default) | Deletes picture bullet for the current list level. |
|[ equals(level)](./equals/#listlevel) | Compares with the specified ListLevel. |
|[ get_effective_value(index, number_style, custom_number_style_format)](./get_effective_value/#int_numberstyle_str) | Reports the string representation of the [ListLevel](./) object for the specified index of the list item. Parameters specify the [NumberStyle](../../aspose.words/numberstyle/) and an optional format string used when [NumberStyle.CUSTOM](../../aspose.words/numberstyle/#CUSTOM) is specified. |

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
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# This NumberFormat value will create star-shaped bullet list symbols.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Create paragraphs and apply both list levels of our custom list formatting to them.
builder = aw.DocumentBuilder(doc)
builder.list_format.list = list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(ARTIFACTS_DIR + 'Lists.create_custom_list.docx')
```

### See Also

* module [aspose.words.lists](../)

