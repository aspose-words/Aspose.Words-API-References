---
title: Run.is_phonetic_guide property
linktitle: is_phonetic_guide property
articleTitle: is_phonetic_guide property
second_title: Aspose.Words for Python
description: "Run.is_phonetic_guide property. Gets a boolean value indicating either the run is a phonetic guide."
type: docs
weight: 20
url: /python-net/aspose.words/run/is_phonetic_guide/
---

## Run.is_phonetic_guide property

Gets a boolean value indicating either the run is a phonetic guide.


```python
@property
def is_phonetic_guide(self) -> bool:
    ...

```

### Examples

Shows how to get properties of the phonetic guide.

```python
doc = aw.Document(file_name=MY_DIR + 'Phonetic guide.docx')
runs = doc.first_section.body.first_paragraph.runs
# Use phonetic guide in the Asian text.
self.assertEqual(True, runs[0].is_phonetic_guide)
phonetic_guide = runs[0].phonetic_guide
self.assertEqual('base', phonetic_guide.base_text)
self.assertEqual('ruby', phonetic_guide.ruby_text)
```

### See Also

* module [aspose.words](../../)
* class [Run](../)

