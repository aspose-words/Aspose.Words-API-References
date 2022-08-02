---
title: ListCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets a list by index."
type: docs
weight: 10
url: /python-net/aspose.words.lists/listcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a list by index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to apply list formatting of an existing list to a collection of paragraphs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Paragraph 1")
builder.writeln("Paragraph 2")
builder.write("Paragraph 3")

paras = [node.as_paragraph() for node in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)]

self.assertEqual(0, len([p for p in paras if p.list_format.is_list_item]))

doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)
list = doc.lists[0]

for paragraph in paras:
    paragraph.list_format.list = list
    paragraph.list_format.list_level_number = 2

self.assertEqual(3, len([p for p in paras if p.list_format.is_list_item]))
```

Shows how to verify owner document properties of lists.

```python
doc = aw.Document()

lists = doc.lists

self.assertEqual(doc, lists.document)

list = lists.add(aw.lists.ListTemplate.BULLET_DEFAULT)

self.assertEqual(doc, list.document)

print("Current list count:", lists.count)
print("Is the first document list:", lists[0] is list)
print("List id:", list.list_id)
print("List is the same by list_id:", lists.get_list_by_list_id(1) is list)
```

### See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

