---
title: Style.list property
linktitle: list property
articleTitle: list property
second_title: Aspose.Words for Python
description: "Style.list property. Gets the list that defines formatting of this list style."
type: docs
weight: 100
url: /python-net/aspose.words/style/list/
---

## Style.list property

Gets the list that defines formatting of this list style.

This property is only valid for list styles.
For other style types this property returns ``None``.




### Examples

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

### See Also

* module [aspose.words](../../)
* class [Style](../)

