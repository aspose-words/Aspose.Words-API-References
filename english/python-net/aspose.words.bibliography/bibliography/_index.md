---
title: Bibliography class
linktitle: Bibliography class
articleTitle: Bibliography class
second_title: Aspose.Words for Python
description: "aspose.words.bibliography.Bibliography class. Represents the list of bibliography sources available in the document."
type: docs
weight: 10
url: /python-net/aspose.words.bibliography/bibliography/
---

## Bibliography class

Represents the list of bibliography sources available in the document.


### Properties

| Name | Description |
| --- | --- |
| [bibliography_style](./bibliography_style/) | Gets a string that represents the name of the active style to use for a bibliography. |
| [sources](./sources/) | Gets a collection that represents all the sources contained in a bibliography. |

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

