---
title: PersonCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "PersonCollection.clear method. Removes all items from the collection."
type: docs
weight: 50
url: /zh/python-net/aspose.words.bibliography/personcollection/clear/
---

## clear() {#default}

Removes all items from the collection.


```python
def clear(self):
    ...
```

### Examples

Shows how to work with person collection.

```python
# 创建一个新的人员集合。
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# 向集合中添加新人员。
persons.add(person)
self.assertEqual(1, persons.count)
# 如果存在，则从集合中移除该人员。
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# 创建包含两个人员的集合。
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# 通过索引从集合中移除人员。
persons.remove_at(0)
self.assertEqual(1, persons.count)
# 从集合中移除所有人员。
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

