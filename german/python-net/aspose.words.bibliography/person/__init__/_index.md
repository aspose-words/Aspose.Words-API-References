---
title: Person constructor
linktitle: Person constructor
articleTitle: Person constructor
second_title: Aspose.Words for Python
description: "Person constructor. Initialize a new instance of the [Person](../) class."
type: docs
weight: 10
url: /de/python-net/aspose.words.bibliography/person/__init__/
---

## Person(last, first, middle) {#str_str_str}

Initialize a new instance of the [Person](../) class.



```python
def __init__(self, last: str, first: str, middle: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| last | str | The last name. |
| first | str | The last name. |
| middle | str | The last name. |

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
* class [Person](../)

