---
title: ContributorCollection class
linktitle: ContributorCollection class
articleTitle: ContributorCollection class
second_title: Aspose.Words for Python
description: "aspose.words.bibliography.ContributorCollection class. Represents bibliography source contributors."
type: docs
weight: 30
url: /python-net/aspose.words.bibliography/contributorcollection/
---

## ContributorCollection class

Represents bibliography source contributors.


### Properties

| Name | Description |
| --- | --- |
| [artist](./artist/) | Gets or sets the artist of a source. |
| [author](./author/) | Gets or sets the author of a source. |
| [book_author](./book_author/) | Gets or sets the book author of a source. |
| [compiler](./compiler/) | Gets or sets the compiler of a source. |
| [composer](./composer/) | Gets or sets the composer of a source. |
| [conductor](./conductor/) | Gets or sets the conductor of a source. |
| [counsel](./counsel/) | Gets or sets the counsel of a source. |
| [director](./director/) | Gets or sets the director of a source. |
| [editor](./editor/) | Gets or sets the editor of a source. |
| [interviewee](./interviewee/) | Gets or sets the interviewee of a source. |
| [interviewer](./interviewer/) | Gets or sets the interviewer of a source. |
| [inventor](./inventor/) | Gets or sets the inventor of a source. |
| [performer](./performer/) | Gets or sets the performer of a source. |
| [producer](./producer/) | Gets or sets the producer of a source. |
| [translator](./translator/) | Gets or sets the translator of a source. |
| [writer](./writer/) | Gets or sets the writer of a source. |

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

