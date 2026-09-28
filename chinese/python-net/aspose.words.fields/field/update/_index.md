---
title: Field.update method
linktitle: update method
articleTitle: update method
second_title: Aspose.Words for Python
description: "aspose.words.fields.Field.update method"
type: docs
weight: 1090
url: /zh/python-net/aspose.words.fields/field/update/
---

## update() {#default}

Performs the field update. Throws if the field is being updated already.


```python
def update(self):
    ...
```

## update(ignore_merge_format) {#bool}

Performs a field update. Throws if the field is being updated already.


```python
def update(self, ignore_merge_format: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ignore_merge_format | bool | If ``True`` then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

## Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用文档生成器插入一个字段，以显示未应用任何格式的结果。
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# 我们可以使用字段的属性为字段的结果应用格式。
# 以下是我们可以应用于字段结果的三种格式类型。
# 1 - 数值格式：
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 - 日期/时间格式：
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 - 常规格式：
field = builder.insert_field(field_code='= 25 + 33')
format_obj = field.format
format_obj.general_formats.add(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.add(aw.fields.GeneralFormat.UPPER)
field.update()
index = 0
for general_format in format_obj.general_formats:
    print(f'General format index {index}: {general_format}')
    index += 1
self.assertEqual('= 25 + 33 \\* roman \\* Upper', field.get_field_code())
self.assertEqual('LVIII', field.result)
self.assertEqual(2, len(format_obj.general_formats))
self.assertEqual(aw.fields.GeneralFormat.LOWERCASE_ROMAN, format_obj.general_formats[0])
# 我们可以移除格式，使字段的结果恢复到原始形式。
format_obj.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.remove_at(0)
self.assertEqual(0, len(format_obj.general_formats))
field.update()
self.assertEqual('= 25 + 33  ', field.get_field_code())
self.assertEqual('58', field.result)
self.assertEqual(0, len(format_obj.general_formats))
```

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
include_picture = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INCLUDE_PICTURE, update_field=True).as_field_include_picture()
include_picture.source_full_name = IMAGE_DIR + 'Transparent background logo.png'
include_picture.update(True)
with io.BytesIO() as doc_stream:
    doc.save(stream=doc_stream, save_options=aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX))
    # 我们可以在 LoadOptions 对象中设置标志，以决定是否转换所有 INCLUDEPICTURE 字段
    # 在加载包含这些字段的文档时，将其转换为图像形状。
    load_options = aw.loading.LoadOptions()
    load_options.preserve_include_picture_field = preserve_include_picture_field
    doc = aw.Document(stream=doc_stream, load_options=load_options)
    if preserve_include_picture_field:
        self.assertTrue(any([f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE for f in doc.range.fields]))
        doc.update_fields()
        doc.save(file_name=ARTIFACTS_DIR + 'Field.PreserveIncludePicture.docx')
    else:
        self.assertFalse(any([f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE for f in doc.range.fields]))
```

## See Also

* module [aspose.words.fields](../../)
* class [Field](../)

