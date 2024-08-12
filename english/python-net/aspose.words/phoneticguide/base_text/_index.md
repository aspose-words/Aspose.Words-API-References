---
title: PhoneticGuide.base_text property
linktitle: base_text property
articleTitle: base_text property
second_title: Aspose.Words for Python
description: "PhoneticGuide.base_text property. Gets base text of the phonetic guide."
type: docs
weight: 10
url: /python-net/aspose.words/phoneticguide/base_text/
---

## PhoneticGuide.base_text property

Gets base text of the phonetic guide.


```python
@property
def base_text(self) -> str:
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
* class [PhoneticGuide](../)

