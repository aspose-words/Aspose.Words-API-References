---
title: PersonCollection constructor
linktitle: PersonCollection constructor
articleTitle: PersonCollection constructor
second_title: Aspose.Words for Python
description: "aspose.words.bibliography.PersonCollection constructor"
type: docs
weight: 10
url: /ar/python-net/aspose.words.bibliography/personcollection/__init__/
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
# أنشئ مجموعة أشخاص جديدة.
persons = aw.bibliography.PersonCollection()
person = aw.bibliography.Person('Roxanne', 'Brielle', 'Tejeda_updated')
# أضف شخصًا جديدًا إلى المجموعة.
persons.add(person)
self.assertEqual(1, persons.count)
# احذف الشخص من المجموعة إذا كان موجودًا.
if persons.contains(person):
    persons.remove(person)
self.assertEqual(0, persons.count)
# أنشئ مجموعة أشخاص تحتوي على شخصين.
persons = aw.bibliography.PersonCollection(persons=[aw.bibliography.Person('Roxanne_1', 'Brielle_1', 'Tejeda_1'), aw.bibliography.Person('Roxanne_2', 'Brielle_2', 'Tejeda_2')])
self.assertEqual(2, persons.count)
# احذف الشخص من المجموعة حسب الفهرس.
persons.remove_at(0)
self.assertEqual(1, persons.count)
# احذف جميع الأشخاص من المجموعة.
persons.clear()
self.assertEqual(0, persons.count)
```

## See Also

* module [aspose.words.bibliography](../../)
* class [PersonCollection](../)

