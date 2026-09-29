---
title: Document.normalize_field_types method
linktitle: normalize_field_types method
articleTitle: normalize_field_types method
second_title: Aspose.Words for Python
description: "Document.normalize_field_types method. Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes."
type: docs
weight: 680
url: /sv/python-net/aspose.words/document/normalize_field_types/
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
# Aspose.Words upptäcker automatiskt fälttyper baserat på fältkoder.
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
# Ändra manuellt den råa texten i fältet, vilket bestämmer fältkoden.
field_text = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.RUN, True)[0].as_run()
field_text.text = 'PAGE'
# Att ändra fältkoden har förändrat detta fält till en av en annan typ,
# men fältets typegenskaper visar fortfarande den gamla typen.
self.assertEqual('PAGE', field.get_field_code())
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.end.field_type)
# Uppdatera dessa egenskaper med den här metoden för att visa aktuellt värde.
doc.normalize_field_types()
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.end.field_type)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

