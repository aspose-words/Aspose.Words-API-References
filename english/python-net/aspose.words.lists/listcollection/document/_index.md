---
title: document property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the owner document."
type: docs
weight: 30
url: /python-net/aspose.words.lists/listcollection/document/
---

## ListCollection.document property

Gets the owner document.


### Examples

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

