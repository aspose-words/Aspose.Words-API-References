---
title: Granularity enumeration
linktitle: Granularity enumeration
articleTitle: Granularity enumeration
second_title: Aspose.Words for Python
description: "aspose.words.comparing.Granularity enumeration. Specifies the granularity of changes to track when comparing two documents."
type: docs
weight: 30
url: /python-net/aspose.words.comparing/granularity/
---

## Granularity enumeration

Specifies the granularity of changes to track when comparing two documents.


### Members

| Name | Description |
| --- | --- |
| CHAR_LEVEL |  |
| WORD_LEVEL |  |

### Examples

Shows to specify a granularity while comparing documents.

```python
doc_a = aw.Document()
builder_a = aw.DocumentBuilder(doc_a)
builder_a.writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit")

doc_b = aw.Document()
builder_b = aw.DocumentBuilder(doc_b)
builder_b.writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit")

# Specify whether changes are tracking
# by character ('Granularity.CHAR_LEVEL'), or by word ('Granularity.WORD_LEVEL').
compare_options = aw.comparing.CompareOptions()
compare_options.granularity = granularity

doc_a.compare(doc_b, "author", datetime.now(), compare_options)

# The first document's collection of revision groups contains all the differences between documents.
groups = doc_a.revisions.groups
self.assertEqual(5, groups.count)
```

### See Also

* module [aspose.words.comparing](../)

