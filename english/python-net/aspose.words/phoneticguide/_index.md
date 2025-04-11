---
title: PhoneticGuide class
linktitle: PhoneticGuide class
articleTitle: PhoneticGuide class
second_title: Aspose.Words for Python
description: "aspose.words.PhoneticGuide class. Represents Phonetic Guide."
type: docs
weight: 940
url: /python-net/aspose.words/phoneticguide/
---

## PhoneticGuide class

Represents Phonetic Guide.


### Properties

| Name | Description |
| --- | --- |
| [base_text](./base_text/) | Gets base text of the phonetic guide. |
| [ruby_text](./ruby_text/) | Gets ruby text of the phonetic guide. |

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

* module [aspose.words](../)

