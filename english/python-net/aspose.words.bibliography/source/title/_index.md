---
title: Source.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Source.title property. Gets the title of a source."
type: docs
weight: 460
url: /python-net/aspose.words.bibliography/source/title/
---

## Source.title property

Gets the title of a source.


```python
@property
def title(self) -> str:
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
* class [Source](../)

