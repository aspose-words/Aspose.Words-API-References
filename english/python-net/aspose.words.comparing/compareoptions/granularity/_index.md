---
title: CompareOptions.granularity property
linktitle: granularity property
articleTitle: granularity property
second_title: Aspose.Words for Python
description: "CompareOptions.granularity property. Specifies whether changes are tracked by character or by word."
type: docs
weight: 30
url: /python-net/aspose.words.comparing/compareoptions/granularity/
---

## CompareOptions.granularity property

Specifies whether changes are tracked by character or by word.


```python
@property
def granularity(self) -> aspose.words.comparing.Granularity:
    ...

@granularity.setter
def granularity(self, value: aspose.words.comparing.Granularity):
    ...

```

### Remarks

Default value is [Granularity.WORD_LEVEL](../../granularity/#WORD_LEVEL).



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

* module [aspose.words.comparing](../../)
* class [CompareOptions](../)

