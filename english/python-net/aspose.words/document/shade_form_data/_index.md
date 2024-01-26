---
title: Document.shade_form_data property
linktitle: shade_form_data property
articleTitle: shade_form_data property
second_title: Aspose.Words for Python
description: "Document.shade_form_data property. Specifies whether to turn on the gray shading on form fields."
type: docs
weight: 390
url: /python-net/aspose.words/document/shade_form_data/
---

## Document.shade_form_data property

Specifies whether to turn on the gray shading on form fields.


```python
@property
def shade_form_data(self) -> bool:
    ...

@shade_form_data.setter
def shade_form_data(self, value: bool):
    ...

```

### Examples

Shows how to apply gray shading to form fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Hello world! ")
builder.insert_text_input("My form field", aw.fields.TextFormFieldType.REGULAR, "",
                          "Text contents of form field, which are shaded in grey by default.", 0)

# We can turn the grey shading off, so the bookmarked text will blend in with the other text.
doc.shade_form_data = use_grey_shading
doc.save(ARTIFACTS_DIR + "Document.shade_form_data.docx")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

