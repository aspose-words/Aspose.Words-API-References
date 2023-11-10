---
title: List.is_multi_level property
linktitle: is_multi_level property
articleTitle: is_multi_level property
second_title: Aspose.Words for Python
description: "List.is_multi_level property. Returns ``True`` when the list contains 9 levels; ``False`` when 1 level."
type: docs
weight: 40
url: /python-net/aspose.words.lists/list/is_multi_level/
---

## List.is_multi_level property

Returns ``True`` when the list contains 9 levels; ``False`` when 1 level.



```python
@property
def is_multi_level(self) -> bool:
    ...

```

### Remarks

The lists that you create with Aspose.Words are always multi-level lists and contain 9 levels.

Microsoft Word 2003 and later always create multi-level lists with 9 levels.
But in some documents, created with earlier versions of Microsoft Word you might encounter
lists that have 1 level only.




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

* module [aspose.words.lists](../../)
* class [List](../)

