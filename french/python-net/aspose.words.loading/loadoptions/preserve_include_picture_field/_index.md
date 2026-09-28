---
title: LoadOptions.preserve_include_picture_field property
linktitle: preserve_include_picture_field property
articleTitle: preserve_include_picture_field property
second_title: Aspose.Words for Python
description: "LoadOptions.preserve_include_picture_field property. Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats"
type: docs
weight: 120
url: /fr/python-net/aspose.words.loading/loadoptions/preserve_include_picture_field/
---

## LoadOptions.preserve_include_picture_field property

Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats.
The default value is ``False``.



```python
@property
def preserve_include_picture_field(self) -> bool:
    ...

@preserve_include_picture_field.setter
def preserve_include_picture_field(self, value: bool):
    ...

```

### Remarks

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need
the field to be preserved, for example, if you wish to update it programmatically. Note however that this
approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path
of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.




### Examples

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
include_picture = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INCLUDE_PICTURE, update_field=True).as_field_include_picture()
include_picture.source_full_name = IMAGE_DIR + 'Transparent background logo.png'
include_picture.update(True)
with io.BytesIO() as doc_stream:
    doc.save(stream=doc_stream, save_options=aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX))
    # Nous pouvons définir un indicateur dans un objet LoadOptions pour décider s'il faut convertir tous les champs INCLUDEPICTURE
    # en formes d'image lors du chargement d'un document qui les contient.
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

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

