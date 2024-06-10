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

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a person at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |

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

