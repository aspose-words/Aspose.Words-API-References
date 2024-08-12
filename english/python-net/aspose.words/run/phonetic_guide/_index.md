---
title: Run.phonetic_guide property
linktitle: phonetic_guide property
articleTitle: phonetic_guide property
second_title: Aspose.Words for Python
description: "Run.phonetic_guide property. Gets a [Run.phonetic_guide](./) object."
type: docs
weight: 40
url: /python-net/aspose.words/run/phonetic_guide/
---

## Run.phonetic_guide property

Gets a [Run.phonetic_guide](./) object.



```python
@property
def phonetic_guide(self) -> aspose.words.PhoneticGuide:
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

