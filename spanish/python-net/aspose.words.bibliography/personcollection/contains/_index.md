---
title: PersonCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "PersonCollection.contains method. Determines whether the collection contains a specific person."
type: docs
weight: 60
url: /es/python-net/aspose.words.bibliography/personcollection/contains/
---

## contains(person) {#person}

Determines whether the collection contains a specific person.


```python
def contains(self, person: aspose.words.bibliography.Person):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| person | [Person](../../person/) | The person to locate in the collection. |

### Examples

Shows how to work with person collection.

```python
# Crea una nueva colección de personas.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Agrega una nueva persona a la colección.
persons.add(person)
self.assertEqual(1, persons.count)
# Elimina la persona de la colección si existe.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# Crea una colección de personas con dos personas.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Elimina la persona de la colección por índice.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Elimina todas las personas de la colección.
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

