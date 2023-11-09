---
title: ListFormat.is_list_item property
linktitle: is_list_item property
articleTitle: is_list_item property
second_title: Aspose.Words for Python
description: "ListFormat.is_list_item property. True when the paragraph has bulleted or numbered formatting applied to it."
type: docs
weight: 10
url: /python-net/aspose.words.lists/listformat/is_list_item/
---

## ListFormat.is_list_item property

True when the paragraph has bulleted or numbered formatting applied to it.


```python
@property
def is_list_item(self) -> bool:
    ...

```

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

Shows how to output all paragraphs in a document that are list items.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.list_format.apply_number_default()
builder.writeln("Numbered list item 1")
builder.writeln("Numbered list item 2")
builder.writeln("Numbered list item 3")
builder.list_format.remove_numbers()

builder.list_format.apply_bullet_default()
builder.writeln("Bulleted list item 1")
builder.writeln("Bulleted list item 2")
builder.writeln("Bulleted list item 3")
builder.list_format.remove_numbers()

paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)

for para in paras:
    para = para.as_paragraph()
    if para.list_format.is_list_item:
        print(f"This paragraph belongs to list ID# {para.list_format.list.list_id}, number style \"{para.list_format.list_level.number_style}\"")
        print(f"\t\"{para.get_text().strip()}\"")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

