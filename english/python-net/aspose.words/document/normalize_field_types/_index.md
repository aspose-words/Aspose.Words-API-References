---
title: Document.normalize_field_types method
linktitle: normalize_field_types method
articleTitle: normalize_field_types method
second_title: Aspose.Words for Python
description: "Document.normalize_field_types method. Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes."
type: docs
weight: 670
url: /python-net/aspose.words/document/normalize_field_types/
---

## normalize_field_types() {#default}

Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/)
in the whole document so that they correspond to the field types contained in the field codes.



```python
def normalize_field_types(self):
    ...
```

### Remarks

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [Range.normalize_field_types()](../../range/normalize_field_types/#default).




### Examples

Shows how to get the keep a field's type up to date with its field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code='DATE', field_value=None)
# Aspose.Words automatically detects field types based on field codes.
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
# Manually change the raw text of the field, which determines the field code.
field_text = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.RUN, True)[0].as_run()
field_text.text = 'PAGE'
# Changing the field code has changed this field to one of a different type,
# but the field's type properties still display the old type.
self.assertEqual('PAGE', field.get_field_code())
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.end.field_type)
# Update those properties with this method to display current value.
doc.normalize_field_types()
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.end.field_type)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

