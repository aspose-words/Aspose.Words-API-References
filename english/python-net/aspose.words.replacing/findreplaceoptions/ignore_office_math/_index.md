---
title: FindReplaceOptions.ignore_office_math property
linktitle: ignore_office_math property
articleTitle: ignore_office_math property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_office_math property. Gets or sets a boolean value indicating either to ignore text inside OfficeMath/>"
type: docs
weight: 110
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_office_math/
---

## FindReplaceOptions.ignore_office_math property

Gets or sets a boolean value indicating either to ignore text inside OfficeMath/\>.
The default value is ``True``.



```python
@property
def ignore_office_math(self) -> bool:
    ...

@ignore_office_math.setter
def ignore_office_math(self, value: bool):
    ...

```

### Examples

Shows how to find and replace text within OfficeMath.

```python
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
self.assertEqual('i+b-c≥iM+bM-cM', doc.first_section.body.first_paragraph.get_text().strip())
options = aw.replacing.FindReplaceOptions()
options.ignore_office_math = is_ignore_office_math
doc.range.replace(pattern='b', replacement='x', options=options)
if is_ignore_office_math:
    self.assertEqual('i+b-c≥iM+bM-cM', doc.first_section.body.first_paragraph.get_text().strip())
else:
    self.assertEqual('i+x-c≥iM+xM-cM', doc.first_section.body.first_paragraph.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

