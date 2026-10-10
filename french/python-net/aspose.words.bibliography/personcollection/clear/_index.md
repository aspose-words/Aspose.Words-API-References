---
title: PersonCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "PersonCollection.clear method. Removes all items from the collection."
type: docs
weight: 50
url: /fr/python-net/aspose.words.bibliography/personcollection/clear/
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

