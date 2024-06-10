---
title: ContributorCollection.author property
linktitle: author property
articleTitle: author property
second_title: Aspose.Words for Python
description: "ContributorCollection.author property. Gets the author of a source."
type: docs
weight: 20
url: /python-net/aspose.words.bibliography/contributorcollection/author/
---

## ContributorCollection.author property

Gets the author of a source.


```python
@property
def author(self) -> aspose.words.bibliography.Contributor:
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
* class [ContributorCollection](../)

