---
title: OoxmlSaveOptions constructor
linktitle: OoxmlSaveOptions constructor
articleTitle: OoxmlSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.OoxmlSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/ooxmlsaveoptions/__init__/
---

## OoxmlSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX) format.



```python
def __init__(self):
    ...
```

## OoxmlSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX),
[SaveFormat.DOCM](../../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../../aspose.words/saveformat/#DOTM) or
[SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# If we configure compatibility options to comply with Microsoft Word 2003,
# inserting an image will define its shape using VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(IMAGE_DIR + "Transparent background logo.png")

self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)

# The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
# If we set the "compliance" property of the SaveOptions object to "OoxmlCompliance.ISO29500_2008_STRICT",
# any document we save while passing this object will have to follow that standard.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX

doc.save(ARTIFACTS_DIR + "OoxmlSaveOptions.iso29500_strict.docx", save_options)

# Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = aw.Document(ARTIFACTS_DIR + "OoxmlSaveOptions.iso29500_strict.docx")

self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

Shows how to support legacy control characters when converting to .docx.

```python
doc = aw.Document(MY_DIR + "Legacy control character.doc")

# When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
# and then pass it to the document's saving method to modify how we save the document.
# Set the "keep_legacy_control_chars" property to "True" to preserve
# the "ShortDateTime" legacy character while saving.
# Set the "keep_legacy_control_chars" property to "False" to remove
# the "ShortDateTime" legacy character from the output document.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.keep_legacy_control_chars = keep_legacy_control_chars

doc.save(ARTIFACTS_DIR + "OoxmlSaveOptions.keep_legacy_control_chars.docx", save_options)

doc = aw.Document(ARTIFACTS_DIR + "OoxmlSaveOptions.keep_legacy_control_chars.docx")

self.assertEqual(
    "\u0013date \\@ \"d/MM/yyyy\"\u0014\u0015\f" if keep_legacy_control_chars else "\u001e\f",
    doc.first_section.body.get_text())
```

## See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

