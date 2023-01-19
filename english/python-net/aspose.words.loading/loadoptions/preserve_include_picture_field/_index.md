---
title: preserve_include_picture_field property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats"
type: docs
weight: 120
url: /python-net/aspose.words.loading/loadoptions/preserve_include_picture_field/
---

## LoadOptions.preserve_include_picture_field property

Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats.
The default value is ``False``.


By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need
the field to be preserved, for example, if you wish to update it programmatically. Note however that this
approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path
of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.




### Examples

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

include_picture = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE_PICTURE, True).as_field_include_picture()
include_picture.source_full_name = IMAGE_DIR + "Transparent background logo.png"
include_picture.update(True)

with io.BytesIO() as doc_stream:

    doc.save(doc_stream, aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX))

    # We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
    # into image shapes when loading a document that contains them.
    load_options = aw.loading.LoadOptions()
    load_options.preserve_include_picture_field = preserve_include_picture_field

    doc = aw.Document(doc_stream, load_options)

    if preserve_include_picture_field:
        self.assertTrue(any(f for f in doc.range.fields if f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE))

        doc.update_fields()
        doc.save(ARTIFACTS_DIR + "Field.preserve_include_picture.docx")
    else:
        self.assertFalse(any(f for f in doc.range.fields if f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE))
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

