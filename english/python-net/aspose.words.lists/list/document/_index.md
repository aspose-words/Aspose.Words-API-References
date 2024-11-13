---
title: List.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "List.document property. Gets the owner document."
type: docs
weight: 10
url: /python-net/aspose.words.lists/list/document/
---

## List.document property

Gets the owner document.


```python
@property
def document(self) -> aspose.words.DocumentBase:
    ...

```

### Remarks

A list always has a parent document and is valid only in the context of that document.




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
* class [List](../)

