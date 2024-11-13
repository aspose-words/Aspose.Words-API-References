---
title: Field.update method
linktitle: update method
articleTitle: update method
second_title: Aspose.Words for Python
description: "aspose.words.fields.Field.update method"
type: docs
weight: 1090
url: /python-net/aspose.words.fields/field/update/
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
builder = aw.DocumentBuilder(doc)
# Use a document builder to insert a field that displays a result with no format applied.
field = builder.insert_field('= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# We can apply a format to a field's result using the field's properties.
# Below are three types of formats that we can apply to a field's result.
# 1 -  Numeric format:
format = field.format
format.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 -  Date/time format:
field = builder.insert_field('DATE')
format = field.format
format.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format.date_time_format} format:\n\t{field.result}")
# 3 -  General format:
field = builder.insert_field('= 25 + 33')
format = field.format
format.general_formats.add(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format.general_formats.add(aw.fields.GeneralFormat.UPPER)
field.update()
for index, general_format in enumerate(format.general_formats):
    print(f'General format index {index}: {general_format}')
self.assertEqual('= 25 + 33 \\* roman \\* Upper', field.get_field_code())
self.assertEqual('LVIII', field.result)
self.assertEqual(2, format.general_formats.count)
self.assertEqual(aw.fields.GeneralFormat.LOWERCASE_ROMAN, format.general_formats[0])
# We can remove our formats to revert the field's result to its original form.
format.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format.general_formats.remove_at(0)
self.assertEqual(0, format.general_formats.count)
field.update()
self.assertEqual('= 25 + 33  ', field.get_field_code())
self.assertEqual('58', field.result)
self.assertEqual(0, format.general_formats.count)
```

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
include_picture = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE_PICTURE, True).as_field_include_picture()
include_picture.source_full_name = IMAGE_DIR + 'Transparent background logo.png'
include_picture.update(True)
with io.BytesIO() as doc_stream:
    doc.save(doc_stream, aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX))
    # We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    # into image shapes when loading a document that contains them.
    load_options = aw.loading.LoadOptions()
    load_options.preserve_include_picture_field = preserve_include_picture_field
    doc = aw.Document(doc_stream, load_options)
    if preserve_include_picture_field:
        self.assertTrue(any((f for f in doc.range.fields if f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE)))
        doc.update_fields()
        doc.save(ARTIFACTS_DIR + 'Field.preserve_include_picture.docx')
    else:
        self.assertFalse(any((f for f in doc.range.fields if f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE)))
```

## See Also

* module [aspose.words.fields](../../)
* class [Field](../)

