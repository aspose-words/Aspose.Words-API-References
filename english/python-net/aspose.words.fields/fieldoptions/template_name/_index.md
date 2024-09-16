---
title: FieldOptions.template_name property
linktitle: template_name property
articleTitle: template_name property
second_title: Aspose.Words for Python
description: "FieldOptions.template_name property. Gets or sets the file name of the template used by the document."
type: docs
weight: 180
url: /python-net/aspose.words.fields/fieldoptions/template_name/
---

## FieldOptions.template_name property

Gets or sets the file name of the template used by the document.


```python
@property
def template_name(self) -> str:
    ...

@template_name.setter
def template_name(self, value: str):
    ...

```

### Remarks

This property is used by the [FieldTemplate](../../fieldtemplate/) field if the [Document.attached_template](../../../aspose.words/document/attached_template/) property is empty.

If this property is empty, the default template file name ``Normal.dotm`` is used.




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
* class [FieldOptions](../)

