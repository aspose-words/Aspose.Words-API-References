---
title: ListCollection.get_list_by_list_id method
linktitle: get_list_by_list_id method
articleTitle: get_list_by_list_id method
second_title: Aspose.Words for Python
description: "ListCollection.get_list_by_list_id method. Gets a list by a list identifier."
type: docs
weight: 70
url: /python-net/aspose.words.lists/listcollection/get_list_by_list_id/
---

## get_list_by_list_id(list_id) {#int}

Gets a list by a list identifier.


```python
def get_list_by_list_id(self, list_id: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_id | int | The list identifier. |

### Remarks

You don't normally need to use this method. Most of the time you apply list formatting
to paragraphs just by settings the [ListFormat.list](../../listformat/list/) property
of the [ListFormat](../../listformat/) object.




### Returns

Returns the list object. Returns ``None`` if a list with the specified identifier was not found.


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

