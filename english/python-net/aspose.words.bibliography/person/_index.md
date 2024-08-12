---
title: Person class
linktitle: Person class
articleTitle: Person class
second_title: Aspose.Words for Python
description: "aspose.words.bibliography.Person class. Represents individual (a person) bibliography source contributor."
type: docs
weight: 50
url: /python-net/aspose.words.bibliography/person/
---

## Person class

Represents individual (a person) bibliography source contributor.


### Constructors
| Name | Description |
| --- | --- |
| [Person(last, first, middle)](./__init__/#str_str_str) | Initialize a new instance of the [Person](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [first](./first/) | Gets or sets the first name of a person. |
| [last](./last/) | Gets or sets the last name of a person. |
| [middle](./middle/) | Gets or sets the middle name of a person. |

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

