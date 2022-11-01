---
title: ListFormat class
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to control what list formatting is applied to a paragraph"
type: docs
weight: 30
url: /python-net/aspose.words.lists/listformat/
---

## ListFormat class

Allows to control what list formatting is applied to a paragraph.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/net/working-with-lists/) documentation article.




A paragraph in a Microsoft Word document can be bulleted or numbered.
When a paragraph is bulleted or numbered, it is said that list formatting
is applied to the paragraph.

You do not create objects of the [ListFormat](./) class directly.
You access [ListFormat](./) as a property of another object that can
have list formatting associated with it. At the moment the objects that can
have list formatting are: [Paragraph](../../aspose.words/paragraph/),
[Style](../../aspose.words/style/) and [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies
what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable
to paragraph styles only) allows to specify what list formatting and list level
is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/)
provides access to the list formatting at the current cursor position
inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

The list formatting itself is stored inside a [List](../list/)
object that is stored separately from the paragraphs. The list objects
are stored inside a [ListCollection](../listcollection/) collection. There is a single
[ListCollection](../listcollection/) collection per [Document](../../aspose.words/document/).

The paragraphs do not physically belong to a list. The paragraphs just
reference a particular list object via the [ListFormat.list](./list/) property
and a particular level in the list via the [ListFormat.list_level_number](./list_level_number/) property.
By setting these two properties you control what bullets and numbering is
applied to a paragraph.




### Properties

| Name | Description |
| --- | --- |
| [is_list_item](./is_list_item/) | True when the paragraph has bulleted or numbered formatting applied to it. |
| [list](./list/) | Gets or sets the list this paragraph is a member of. |
| [list_level](./list_level/) | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [list_level_number](./list_level_number/) | Gets or sets the list level number (0 to 8) for the paragraph. |

### Methods

| Name | Description |
| --- | --- |
|[ apply_bullet_default()](./apply_bullet_default/#default) | Starts a new default bulleted list and applies it to the paragraph. |
|[ apply_number_default()](./apply_number_default/#default) | Starts a new default numbered list and applies it to the paragraph. |
|[ list_indent()](./list_indent/#default) | Increases the list level of the current paragraph by one level. |
|[ list_outdent()](./list_outdent/#default) | Decreases the list level of the current paragraph by one level. |
|[ remove_numbers()](./remove_numbers/#default) | Removes numbers or bullets from the current paragraph and sets list level to zero. |

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

### See Also

* module [aspose.words.lists](../)

