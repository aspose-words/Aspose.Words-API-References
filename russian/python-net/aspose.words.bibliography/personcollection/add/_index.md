---
title: PersonCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "PersonCollection.add method. Adds a [Person](../../person/) to the collection."
type: docs
weight: 40
url: /ru/python-net/aspose.words.bibliography/personcollection/add/
---

## add(person) {#person}

Adds a [Person](../../person/) to the collection.



```python
def add(self, person: aspose.words.bibliography.Person):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| person | [Person](../../person/) | The person to add to the collection. |

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

