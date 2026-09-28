---
title: Range.delete method
linktitle: delete method
articleTitle: delete method
second_title: Aspose.Words for Python
description: "Range.delete method. Deletes all characters of the range."
type: docs
weight: 70
url: /zh/python-net/aspose.words/range/delete/
---

## delete() {#default}

Deletes all characters of the range.


```python
def delete(self):
    ...
```

### Examples

Shows how to delete all the nodes from a range.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 向文档的第一个节添加文本，然后再添加另一个节。
builder.write('Section 1. ')
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.write('Section 2.')
self.assertEqual('Section 1. \x0cSection 2.', doc.get_text().strip())
# 通过删除所有节点来完全移除第一个节
# 在其范围内，包括该节本身。
doc.sections[0].range.delete()
self.assertEqual(1, doc.sections.count)
self.assertEqual('Section 2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Range](../)

