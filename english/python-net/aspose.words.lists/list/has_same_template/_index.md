---
title: List.has_same_template method
linktitle: has_same_template method
articleTitle: has_same_template method
second_title: Aspose.Words for Python
description: "List.has_same_template method. Returns true if the current list and the given list are created from the same template."
type: docs
weight: 110
url: /python-net/aspose.words.lists/list/has_same_template/
---

## has_same_template(other) {#list}

Returns true if the current list and the given list are created from the same template.


```python
def has_same_template(self, other: aspose.words.lists.List):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| other | [List](../) |  |

### Examples

Shows how to define lists with the same ListDefId.

```python
doc = aw.Document(MY_DIR + "Different lists.docx");

self.assertTrue(doc.lists[0].has_same_template(doc.lists[1]))
self.assertFalse(doc.lists[1].has_same_template(doc.lists[2]))
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)

