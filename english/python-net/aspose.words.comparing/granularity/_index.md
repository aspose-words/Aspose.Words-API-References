---
title: Granularity enumeration
linktitle: Granularity enumeration
articleTitle: Granularity enumeration
second_title: Aspose.Words for Python
description: "aspose.words.comparing.Granularity enumeration. Specifies the granularity of changes to track when comparing two documents."
type: docs
weight: 40
url: /python-net/aspose.words.comparing/granularity/
---

## Granularity enumeration

Specifies the granularity of changes to track when comparing two documents.


### Members

| Name | Description |
| --- | --- |
| CHAR_LEVEL | Specifies changes at the character level. |
| WORD_LEVEL | Specifies changes at the word level. |

### Examples

Shows to specify a granularity while comparing documents.

```python
doc_a = aw.Document()
builder_a = aw.DocumentBuilder(doc=doc_a)
builder_a.writeln('Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit')
doc_b = aw.Document()
builder_b = aw.DocumentBuilder(doc=doc_b)
builder_b.writeln('Lorems ipsum dolor sit amet consectetur - "adipiscing" elit')
# Specify whether changes are tracking
# by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
compare_options = aw.comparing.CompareOptions()
compare_options.granularity = granularity
doc_a.compare(document=doc_b, author='author', date_time=datetime.datetime.now(), options=compare_options)
# The first document's collection of revision groups contains all the differences between documents.
groups = doc_a.revisions.groups
self.assertEqual(5, groups.count)
```

### See Also

* module [aspose.words.comparing](../)

