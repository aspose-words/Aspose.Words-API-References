---
title: PersonCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "PersonCollection.clear method. Removes all items from the collection."
type: docs
weight: 50
url: /ru/python-net/aspose.words.bibliography/personcollection/clear/
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
# Создайте новую коллекцию person.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Добавьте нового person в коллекцию.
persons.add(person)
self.assertEqual(1, persons.count)
# Удалите person из коллекции, если он существует.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# Создайте коллекцию person с двумя объектами.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Удалите person из коллекции по индексу.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Удалите всех person из коллекции.
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

