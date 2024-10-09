---
title: ShapeMarkupLanguage enumeration
linktitle: ShapeMarkupLanguage enumeration
articleTitle: ShapeMarkupLanguage enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ShapeMarkupLanguage enumeration. Specifies Markup language used for the shape."
type: docs
weight: 390
url: /python-net/aspose.words.drawing/shapemarkuplanguage/
---

## ShapeMarkupLanguage enumeration

Specifies Markup language used for the shape.


### Members

| Name | Description |
| --- | --- |
| DML | Drawing Markup Language is used to define the shape. |
| VML | Vector Markup Language is used to define the shape. |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# If we configure compatibility options to comply with Microsoft Word 2003,
# inserting an image will define its shape using VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
# If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
# any document we save while passing this object will have to follow that standard.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

### See Also

* module [aspose.words.drawing](../)

