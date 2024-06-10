---
title: PhoneticGuide.ruby_text property
linktitle: ruby_text property
articleTitle: ruby_text property
second_title: Aspose.Words for Python
description: "PhoneticGuide.ruby_text property. Gets ruby text of the phonetic guide."
type: docs
weight: 20
url: /python-net/aspose.words/phoneticguide/ruby_text/
---

## PhoneticGuide.ruby_text property

Gets ruby text of the phonetic guide.


```python
@property
def ruby_text(self) -> str:
    ...

```

### Examples

Shows how to get properties of the phonetic guide.

```python
doc = aw.Document(file_name=MY_DIR + 'Phonetic guide.docx')
runs = doc.first_section.body.first_paragraph.runs
# Use phonetic guide in the Asian text.
self.assertEqual(True, runs[0].is_phonetic_guide)
self.assertEqual('base', runs[0].phonetic_guide.base_text)
self.assertEqual('ruby', runs[0].phonetic_guide.ruby_text)
```

### See Also

* module [aspose.words](../../)
* class [PhoneticGuide](../)

