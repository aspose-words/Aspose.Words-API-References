﻿---
title: FieldTemplate.include_full_path property
linktitle: include_full_path property
articleTitle: include_full_path property
second_title: Aspose.Words for Python
description: "FieldTemplate.include_full_path property. Gets or sets whether to include the full file path name."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldtemplate/include_full_path/
---

## FieldTemplate.include_full_path property

Gets or sets whether to include the full file path name.


```python
@property
def include_full_path(self) -> bool:
    ...

@include_full_path.setter
def include_full_path(self, value: bool):
    ...

```

### Examples

Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
# If this property is empty the default template file name "Normal.dotm" is used.
doc.field_options.template_name = ''
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TEMPLATE, update_field=False).as_field_template()
self.assertEqual(' TEMPLATE ', field.get_field_code())
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TEMPLATE, update_field=False).as_field_template()
field.include_full_path = True
self.assertEqual(' TEMPLATE  \\p', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TEMPLATE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTemplate](../)

