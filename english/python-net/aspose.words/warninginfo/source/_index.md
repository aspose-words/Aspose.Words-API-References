---
title: WarningInfo.source property
linktitle: source property
articleTitle: source property
second_title: Aspose.Words for Python
description: "WarningInfo.source property. Returns the source of the warning."
type: docs
weight: 20
url: /python-net/aspose.words/warninginfo/source/
---

## WarningInfo.source property

Returns the source of the warning.


```python
@property
def source(self) -> aspose.words.WarningSource:
    ...

```

### Examples

Shows how to work with the warning source.

```python
doc = aw.Document(file_name=MY_DIR + 'Emphases markdown warning.docx')
warnings = aw.WarningInfoCollection()
doc.warning_callback = warnings
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.EmphasesWarningSourceMarkdown.md')
for warning_info in warnings:
    if warning_info.source == aw.WarningSource.MARKDOWN:
        self.assertEqual('The (*, 0:11) cannot be properly written into Markdown.', warning_info.description)
```

### See Also

* module [aspose.words](../../)
* class [WarningInfo](../)

