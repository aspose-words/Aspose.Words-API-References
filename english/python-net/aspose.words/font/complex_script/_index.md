---
title: Font.complex_script property
linktitle: complex_script property
articleTitle: complex_script property
second_title: Aspose.Words for Python
description: "Font.complex_script property. Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run."
type: docs
weight: 80
url: /python-net/aspose.words/font/complex_script/
---

## Font.complex_script property

Specifies whether the contents of this run shall be treated as complex script text regardless
of their Unicode character values when determining the formatting for this run.


```python
@property
def complex_script(self) -> bool:
    ...

@complex_script.setter
def complex_script(self, value: bool):
    ...

```

### Examples

Shows how to add text that is always treated as complex script.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.complex_script = True
builder.writeln('Text treated as complex script.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ComplexScript.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

