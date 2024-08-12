---
title: PersonCollection class
linktitle: PersonCollection class
articleTitle: PersonCollection class
second_title: Aspose.Words for Python
description: "aspose.words.bibliography.PersonCollection class. Represents a list of persons who are bibliography source contributors."
type: docs
weight: 60
url: /python-net/aspose.words.bibliography/personcollection/
---

## PersonCollection class

Represents a list of persons who are bibliography source contributors.


**Inheritance:** [PersonCollection](./) → [Contributor](../contributor/)

### Constructors
| Name | Description |
| --- | --- |
| [PersonCollection()](./__init__/#default) | Initialize a new instance of the [PersonCollection](./) class. |
| [PersonCollection(persons)](./__init__/#person]) |  |
| [PersonCollection(persons)](./__init__/#personlist) | Initialize a new instance of the [PersonCollection](./) class. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets a person at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of persons contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(person)](./add/#person) | Adds a [Person](../person/) to the collection. |
|[ clear()](./clear/#default) | Removes all items from the collection. |
|[ contains(person)](./contains/#person) | Determines whether the collection contains a specific person. |
|[ remove(person)](./remove/#person) | Removes the person from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes the person at the specified index. |

### Examples

Shows how to get bibliography sources available in the document.

```python
document = aw.Document(MY_DIR + 'Bibliography sources.docx')
bibliography = document.bibliography
self.assertEqual(12, len(bibliography.sources))
source = bibliography.sources[0]
self.assertEqual('Book 0 (No LCID)', source.title)
authors = source.contributors.author.as_person_collection()
self.assertEqual(2, authors.count)
person = authors[0]
self.assertEqual('Roxanne', person.first)
self.assertEqual('Brielle', person.middle)
self.assertEqual('Tejeda', person.last)
```

### See Also

* module [aspose.words.bibliography](../)
* class [Contributor](../contributor/)

