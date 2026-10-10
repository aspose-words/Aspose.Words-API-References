---
title: PersonCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "PersonCollection.remove_at method. Removes the person at the specified index."
type: docs
weight: 80
url: /it/python-net/aspose.words.bibliography/personcollection/remove_at/
---

## remove_at(index) {#int}

Removes the person at the specified index.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the person to remove. |

### Examples

Shows how to work with person collection.

```python
# Crea una nuova collezione di persone.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Aggiungi una nuova persona alla collezione.
persons.add(person)
self.assertEqual(1, persons.count)
# Rimuovi la persona dalla collezione se esiste.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# Crea una collezione di persone con due persone.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Rimuovi la persona dalla collezione per indice.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Rimuovi tutte le persone dalla collezione.
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

