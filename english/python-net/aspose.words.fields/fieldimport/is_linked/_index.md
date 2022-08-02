---
title: is_linked property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets whether to reduce the file size by not storing graphics data with the document."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldimport/is_linked/
---

## FieldImport.is_linked property

Gets or sets whether to reduce the file size by not storing graphics data with the document.


### Examples

Shows how to insert images using IMPORT and INCLUDEPICTURE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two similar field types that we can use to display images linked from the local file system.
# 1 -  The INCLUDEPICTURE field:
field_include_picture = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE_PICTURE, True).as_field_include_picture()
field_include_picture.source_full_name = IMAGE_DIR + "Transparent background logo.png"

self.assertRegex(field_include_picture.get_field_code(), " INCLUDEPICTURE  .*")

# Apply the PNG32.FLT filter.
field_include_picture.graphic_filter = "PNG32"
field_include_picture.is_linked = True
field_include_picture.resize_horizontally = True
field_include_picture.resize_vertically = True

# 2 -  The IMPORT field:
field_import = builder.insert_field(aw.fields.FieldType.FIELD_IMPORT, True).as_field_import()
field_import.source_full_name = IMAGE_DIR + "Transparent background logo.png"
field_import.graphic_filter = "PNG32"
field_import.is_linked = True

self.assertRegex(field_import.get_field_code(), r" IMPORT  .* \\c PNG32 \\d")

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_include_picture.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldImport](../)

