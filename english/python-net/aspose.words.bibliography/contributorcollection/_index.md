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
| [artist](./artist/) | Gets the artist of a source. |
| [author](./author/) | Gets the author of a source. |
| [book_author](./book_author/) | Gets the book author of a source. |
| [compiler](./compiler/) | Gets the compiler of a source. |
| [composer](./composer/) | Gets the composer of a source. |
| [conductor](./conductor/) | Gets the conductor of a source. |
| [counsel](./counsel/) | Gets the counsel of a source. |
| [director](./director/) | Gets the director of a source. |
| [editor](./editor/) | Gets the editor of a source. |
| [interviewee](./interviewee/) | Gets the interviewee of a source. |
| [interviewer](./interviewer/) | Gets the interviewer of a source. |
| [inventor](./inventor/) | Gets the inventor of a source. |
| [performer](./performer/) | Gets the performer of a source. |
| [producer](./producer/) | Gets the producer of a source. |
| [translator](./translator/) | Gets the translator of a source. |
| [writer](./writer/) | Gets the writer of a source. |

### Examples

Shows how to get bibliography sources available in the document.

```python
document = aw.Document(MY_DIR + "Bibliography sources.docx")

bibliography = document.bibliography
self.assertEqual(12, len(bibliography.sources))

source = bibliography.sources[0]
self.assertEqual("Book 0 (No LCID)", source.title)

authors = source.contributors.author.as_person_collection()
self.assertEqual(2, authors.count)

person = authors[0]
self.assertEqual("Roxanne", person.first)
self.assertEqual("Brielle", person.middle)
self.assertEqual("Tejeda", person.last)
```

### See Also

* module [aspose.words.bibliography](../)

