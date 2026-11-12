---
title: PersonCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "PersonCollection.add method. Adds a [Person](../../person/) to the collection."
type: docs
weight: 40
url: /tr/python-net/aspose.words.bibliography/personcollection/add/
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
# Yeni bir kişi koleksiyonu oluştur.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Koleksiyona yeni bir kişi ekle.
persons.add(person)
self.assertEqual(1, persons.count)
# Koleksiyonda varsa kişiyi kaldır.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# İki kişilik bir kişi koleksiyonu oluştur.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Koleksiyondan indekse göre kişiyi kaldır.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Koleksiyondaki tüm kişileri kaldır.
persons.clear()
self.assertEqual(0, persons.count)
```

### See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

