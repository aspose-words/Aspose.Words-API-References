---
title: ListCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListCollection.add method"
type: docs
weight: 40
url: /python-net/aspose.words.lists/listcollection/add/
---

## add(list_template) {#listtemplate}

Creates a new list based on a predefined template and adds it to the collection of lists in the document.


```python
def add(self, list_template: aspose.words.lists.ListTemplate):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_template | [ListTemplate](../../listtemplate/) |  |

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.

All lists created using this method have 9 list levels.




### Returns

The newly created list.


## add(list_style) {#style}

Creates a new list that references a list style and adds it to the collection of lists in the document.


```python
def add(self, list_style: aspose.words.Style):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_style | [Style](../../../aspose.words/style/) |  |

The newly created list references the list style. If you change the properties of the list
style, it is reflected in the properties of the list. Vice versa, if you change the properties
of the list, it is reflected in the properties of the list style.




### Returns

The newly created list.


## Examples

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

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Create a list from a Microsoft Word template, and customize its first list level.
list1 = doc.lists.add(aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = drawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT

# Apply our list to some paragraphs.
builder = aw.DocumentBuilder(doc)

builder.writeln("List 1 starts below:")
builder.list_format.list = list1
builder.writeln("Item 1")
builder.writeln("Item 2")
builder.list_format.remove_numbers()

# We can add a copy of an existing list to the document's list collection
# to create a similar list without making changes to the original.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = drawing.Color.blue
list2.list_levels[0].start_at = 10

# Apply the second list to new paragraphs.
builder.writeln("List 2 starts below:")
builder.list_format.list = list2
builder.writeln("Item 1")
builder.writeln("Item 2")
builder.list_format.remove_numbers()

doc.save(ARTIFACTS_DIR + "Lists.restart_numbering_using_list_copy.docx")
```

Shows how to create a list by applying a new list format to a collection of paragraphs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Paragraph 1")
builder.writeln("Paragraph 2")
builder.write("Paragraph 3")

paras = [node.as_paragraph() for node in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)]

self.assertEqual(0, len([p for p in paras if p.list_format.is_list_item]))

list = doc.lists.add(aw.lists.ListTemplate.NUMBER_UPPERCASE_LETTER_DOT)

for paragraph in paras:
    paragraph.list_format.list = list
    paragraph.list_format.list_level_number = 1

self.assertEqual(3, len([p for p in paras if p.list_format.is_list_item]))
```

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# We can contain an entire List object within a style.
list_style = doc.styles.add(aw.StyleType.LIST, "MyListStyle")

list1 = list_style.list

self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)

# Change the appearance of all list levels in our list.
for level in list1.list_levels:
    level.font.name = "Verdana"
    level.font.color = drawing.Color.blue
    level.font.bold = True

builder = aw.DocumentBuilder(doc)

builder.writeln("Using list style first time:")

# Create another list from a list within a style.
list2 = doc.lists.add(list_style)

self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)

# Add some list items that our list will format.
builder.list_format.list = list2
builder.writeln("Item 1")
builder.writeln("Item 2")
builder.list_format.remove_numbers()

builder.writeln("Using list style second time:")

# Create and apply another list based on the list style.
list3 = doc.lists.add(list_style)
builder.list_format.list = list3
builder.writeln("Item 1")
builder.writeln("Item 2")
builder.list_format.remove_numbers()

builder.document.save(ARTIFACTS_DIR + "Lists.create_and_use_list_style.docx")
```

## See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

