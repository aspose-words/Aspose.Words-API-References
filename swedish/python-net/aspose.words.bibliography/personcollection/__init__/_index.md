---
title: PersonCollection constructor
linktitle: PersonCollection constructor
articleTitle: PersonCollection constructor
second_title: Aspose.Words for Python
description: "aspose.words.bibliography.PersonCollection constructor"
type: docs
weight: 10
url: /sv/python-net/aspose.words.bibliography/personcollection/__init__/
---

## PersonCollection() {#default}

Initialize a new instance of the [PersonCollection](../) class.



```python
def __init__(self):
    ...
```

## PersonCollection(persons) {#person]}

```python
def __init__(self, persons: Iterable[aspose.words.bibliography.Person]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| persons | Iterable[[Person](../../person/)] |  |

## PersonCollection(persons) {#personlist}

Initialize a new instance of the [PersonCollection](../) class.



```python
def __init__(self, persons: List[aspose.words.bibliography.Person]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| persons | List[[Person](../../person/)] |  |

## Examples

Shows how to work with person collection.

```python
# Skapa en ny personsamling.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# Lägg till en ny person i samlingen.
persons.add(person)
self.assertEqual(1, persons.count)
# Ta bort personen från samlingen om den finns.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# Skapa en personsamling med två personer.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# Ta bort personen från samlingen efter indexet.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# Ta bort alla personer från samlingen.
persons.clear()
self.assertEqual(0, persons.count)
```

## See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

