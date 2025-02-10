---
title: ListCollection indexer
linktitle: ListCollection indexer
articleTitle: ListCollection indexer
second_title: Aspose.Words for Python
description: "ListCollection indexer. Gets a list by index."
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
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1')
builder.writeln('Paragraph 2')
builder.write('Paragraph 3')
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
doc_list = doc.lists[0]
for paragraph in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras))):
    paragraph.list_format.list = doc_list
    paragraph.list_format.list_level_number = 2
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

Shows how to verify owner document properties of lists.

```python
doc = aw.Document()
lists = doc.lists
self.assertEqual(doc, lists.document)
list = lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
self.assertEqual(doc, list.document)
print('Current list count: ' + str(lists.count))
print('Is the first document list: ' + str(lists[0].equals(list=list)))
print('ListId: ' + str(list.list_id))
print('List is the same by ListId: ' + str(lists.get_list_by_list_id(1).equals(list=list)))
```

### See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

