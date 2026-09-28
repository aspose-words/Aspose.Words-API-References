---
title: Range.normalize_field_types method
linktitle: normalize_field_types method
articleTitle: normalize_field_types method
second_title: Aspose.Words for Python
description: "Range.normalize_field_types method. Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) in this range so that they correspond to the field types contained in the field codes."
type: docs
weight: 80
url: /zh/python-net/aspose.words/range/normalize_field_types/
---

## normalize_field_types() {#default}

Changes field type values [FieldChar.field_type](../../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/)
in this range so that they correspond to the field types contained in the field codes.



```python
def normalize_field_types(self):
    ...
```

### Remarks

Use this method after document changes that affect field types.

To change field type values in the whole document use [Document.normalize_field_types()](../../document/normalize_field_types/#default).




### Examples

Shows how to get the keep a field's type up to date with its field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_code='DATE', field_value=None)
# Aspose.Words 会根据字段代码自动检测字段类型。
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
# 手动更改字段的原始文本，该文本决定字段代码。
field_text = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.RUN, True)[0].as_run()
field_text.text = 'PAGE'
# 更改字段代码已将此字段更改为另一种类型，
# 但字段的类型属性仍显示旧类型。
self.assertEqual('PAGE', field.get_field_code())
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.end.field_type)
# 使用此方法更新这些属性以显示当前值。
doc.normalize_field_types()
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.start.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.separator.field_type)
self.assertEqual(aw.fields.FieldType.FIELD_PAGE, field.end.field_type)
```

### See Also

* module [aspose.words](../../)
* class [Range](../)

