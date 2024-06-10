---
title: ViewOptions.forms_design property
linktitle: forms_design property
articleTitle: forms_design property
second_title: Aspose.Words for Python
description: "ViewOptions.forms_design property. Specifies whether the document is in forms design mode."
type: docs
weight: 30
url: /python-net/aspose.words.settings/viewoptions/forms_design/
---

## ViewOptions.forms_design property

Specifies whether the document is in forms design mode.


```python
@property
def forms_design(self) -> bool:
    ...

@forms_design.setter
def forms_design(self, value: bool):
    ...

```

### Remarks

Currently works only for documents in WordML format.




### Examples

Shows how to enable/disable forms design mode.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
# Set the "forms_design" property to "False" to keep forms design mode disabled.
# Set the "forms_design" property to "True" to enable forms design mode.
doc.view_options.forms_design = use_forms_design
doc.save(ARTIFACTS_DIR + 'ViewOptions.forms_design.xml')
with open(ARTIFACTS_DIR + 'ViewOptions.forms_design.xml') as file:
    self.assertEqual(use_forms_design, '<w:formsDesign />' in file.read())
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

