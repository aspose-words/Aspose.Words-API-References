---
title: Source.contributors property
linktitle: contributors property
articleTitle: contributors property
second_title: Aspose.Words for Python
description: "Source.contributors property. Gets contributors list (author, editor, writer etc) of a source."
type: docs
weight: 120
url: /python-net/aspose.words.bibliography/source/contributors/
---

## Source.contributors property

Gets contributors list (author, editor, writer etc) of a source.


```python
@property
def contributors(self) -> aspose.words.bibliography.ContributorCollection:
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

