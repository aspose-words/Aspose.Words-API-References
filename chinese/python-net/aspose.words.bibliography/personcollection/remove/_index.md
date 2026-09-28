---
title: PersonCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "PersonCollection.remove method. Removes the person from the collection."
type: docs
weight: 70
url: /zh/python-net/aspose.words.bibliography/personcollection/remove/
---

## remove(person) {#person}

Removes the person from the collection.


```python
def remove(self, person: aspose.words.bibliography.Person):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| person | [Person](../../person/) | The person to remove from the collection. |

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

