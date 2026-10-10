---
title: PersonCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "PersonCollection.remove method. Removes the person from the collection."
type: docs
weight: 70
url: /de/python-net/aspose.words.bibliography/personcollection/remove/
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
# Erstelle eine neue Personensammlung.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Füge der Sammlung eine neue Person hinzu.
persons.add(person)
self.assertEqual(1, persons.count)
# Entferne die Person aus der Sammlung, falls sie existiert.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# Erstelle eine Personensammlung mit zwei Personen.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Entferne die Person aus der Sammlung anhand des Index.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Entferne alle Personen aus der Sammlung.
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

