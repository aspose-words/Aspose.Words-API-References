---
title: List.is_list_style_definition property
linktitle: is_list_style_definition property
articleTitle: is_list_style_definition property
second_title: Aspose.Words for Python
description: "List.is_list_style_definition property. Returns ``True`` if this list is a definition of a list style."
type: docs
weight: 20
url: /python-net/aspose.words.lists/list/is_list_style_definition/
---

## List.is_list_style_definition property

Returns ``True`` if this list is a definition of a list style.



```python
@property
def is_list_style_definition(self) -> bool:
    ...

```

### Remarks

When this property is ``True``, the [List.style](../style/) property returns the list style that
this list defines.

By modifying properties of a list that defines a list style, you modify the properties
of the list style.

A list that is a definition of a list style cannot be applied directly to paragraphs
to make them numbered.




### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "ListFormat" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# We can contain an entire List object within a style.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Change the appearance of all list levels in our list.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Create another list from a list within a style.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Add some list items that our list will format.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Create and apply another list based on the list style.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)
* property [List.style](../style/)
* property [List.is_list_style_reference](../is_list_style_reference/)

