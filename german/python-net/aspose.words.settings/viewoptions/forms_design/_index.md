---
title: ViewOptions.forms_design property
linktitle: forms_design property
articleTitle: forms_design property
second_title: Aspose.Words for Python
description: "ViewOptions.forms_design property. Specifies whether the document is in forms design mode."
type: docs
weight: 30
url: /de/python-net/aspose.words.settings/viewoptions/forms_design/
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
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Setzen Sie die "FormsDesign"-Eigenschaft auf "false", um den Formular-Designmodus deaktiviert zu lassen.
# Setzen Sie die "FormsDesign"-Eigenschaft auf "true", um den Formular-Designmodus zu aktivieren.
doc.view_options.forms_design = use_forms_design
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.FormsDesign.xml')
self.assertEqual(use_forms_design, '<w:formsDesign />' in system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'ViewOptions.FormsDesign.xml'))
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

