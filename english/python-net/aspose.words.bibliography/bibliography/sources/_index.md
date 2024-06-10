---
title: Bibliography.sources property
linktitle: sources property
articleTitle: sources property
second_title: Aspose.Words for Python
description: "Bibliography.sources property. Gets a collection that represents all the sources contained in a bibliography."
type: docs
weight: 20
url: /python-net/aspose.words.bibliography/bibliography/sources/
---

## Bibliography.sources property

Gets a collection that represents all the sources contained in a bibliography.


```python
@property
def sources(self) -> List[aspose.words.bibliography.Source]:
    ...

```

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

* module [aspose.words.bibliography](../../)
* class [Bibliography](../)

