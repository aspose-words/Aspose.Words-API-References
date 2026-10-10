---
title: PersonCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "PersonCollection.contains method. Determines whether the collection contains a specific person."
type: docs
weight: 60
url: /fr/python-net/aspose.words.bibliography/personcollection/contains/
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
# Créez une nouvelle collection de personnes.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Ajoutez une nouvelle personne à la collection.
persons.add(person)
self.assertEqual(1, persons.count)
# Supprimez la personne de la collection si elle existe.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# Créez une collection de personnes contenant deux personnes.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Supprimez la personne de la collection par son indice.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Supprimez toutes les personnes de la collection.
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

