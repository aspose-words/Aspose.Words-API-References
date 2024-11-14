---
title: ListCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ListCollection.count property. Gets the count of numbered and bulleted lists in the document."
type: docs
weight: 20
url: /python-net/aspose.words.lists/listcollection/count/
---

## ListCollection.count property

Gets the count of numbered and bulleted lists in the document.


```python
@property
def count(self) -> int:
    ...

```

### Examples

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

