---
title: OoxmlCompliance enumeration
linktitle: OoxmlCompliance enumeration
articleTitle: OoxmlCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.OoxmlCompliance enumeration. Allows to specify which OOXML specification will be used when saving in the DOCX format."
type: docs
weight: 510
url: /python-net/aspose.words.saving/ooxmlcompliance/
---

## OoxmlCompliance enumeration

Allows to specify which OOXML specification will be used when saving in the DOCX format.


### Members

| Name | Description |
| --- | --- |
| ECMA376_2006 | ECMA-376 1st Edition, 2006. |
| ISO29500_2008_TRANSITIONAL | ISO/IEC 29500:2008 Transitional compliance level. |
| ISO29500_2008_STRICT | ISO/IEC 29500:2008 Strict compliance level. |

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

Shows how to configure a list to restart numbering at each section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)
list = doc.lists[0]
list.is_restart_at_each_section = restart_list_at_each_section
# The "is_restart_at_each_section" property will only be applicable when
# the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.ECMA376".
options = aw.saving.OoxmlSaveOptions()
options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
builder.list_format.list = list
builder.writeln('List item 1')
builder.writeln('List item 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('List item 3')
builder.writeln('List item 4')
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.restarting_document_list.docx', options)
doc = aw.Document(ARTIFACTS_DIR + 'OoxmlSaveOptions.restarting_document_list.docx')
self.assertEqual(restart_list_at_each_section, doc.lists[0].is_restart_at_each_section)
```

Shows how to insert DML shapes into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Below are two wrapping types that shapes may have.
# 1 -  Floating:
builder.insert_shape(aw.drawing.ShapeType.TOP_CORNERS_ROUNDED, aw.drawing.RelativeHorizontalPosition.PAGE, 100, aw.drawing.RelativeVerticalPosition.PAGE, 100, 50, 50, aw.drawing.WrapType.NONE)
# 2 -  Inline:
builder.insert_shape(aw.drawing.ShapeType.DIAGONAL_CORNERS_ROUNDED, 50, 50)
# If you need to create "non-primitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
# then save the document with "Strict" or "Transitional" compliance, which allows saving shape as DML.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
doc.save(ARTIFACTS_DIR + 'Shape.shape_insertion.docx', save_options)
```

### See Also

* module [aspose.words.saving](../)

