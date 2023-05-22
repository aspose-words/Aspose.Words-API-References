---
title: CompatibilityOptions.optimize_for method
linktitle: optimize_for method
articleTitle: optimize_for method
second_title: Aspose.Words for Python
description: "CompatibilityOptions.optimize_for method. Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word."
type: docs
weight: 720
url: /python-net/aspose.words.settings/compatibilityoptions/optimize_for/
---

## optimize_for(version) {#mswordversion}

Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word.

Use this method to prevent MS Word from displaying "Compatibility mode" ribbon upon document loading.
(Note that you may also need to set the [OoxmlSaveOptions.compliance](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) property to 
[OoxmlCompliance.ISO29500_2008_TRANSITIONAL](../../../aspose.words.saving/ooxmlcompliance/#ISO29500_2008_TRANSITIONAL) or higher.)





```python
def optimize_for(self, version: aspose.words.settings.MsWordVersion):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| version | [MsWordVersion](../../mswordversion/) |  |

### Examples

Shows how to optimize the document for different versions of Microsoft Word.

```python
def test_optimize_for(self):

    doc = aw.Document()

    # This object contains an extensive list of flags unique to each document
    # that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    options = doc.compatibility_options

    # Print the default settings for a blank document.
    print("\nDefault optimization settings:")
    ExCompatibilityOptions.print_compatibility_options(options)

    # We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.save(ARTIFACTS_DIR + "CompatibilityOptions.optimize_for.default_settings.docx")

    # We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2010)
    print("\nOptimized for Word 2010:")
    ExCompatibilityOptions.print_compatibility_options(options)

    doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2000)
    print("\nOptimized for Word 2000:")
    ExCompatibilityOptions.print_compatibility_options(options)

@staticmethod
def print_compatibility_options(options: aw.settings.CompatibilityOptions):
    """Groups all flags in a document's compatibility options object by state, then prints each group."""

    for enabled in (True, False):
        print("\tEnabled options:" if enabled else "\tDisabled options:")
        for opt in dir(options):
            if not opt.startswith('__') and not callable(getattr(options, opt)) and getattr(options, opt) == enabled:
                print(f"\t\t{opt}")
```

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

Shows how to vertically align the text contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 200, 200)

# Set the "vertical_anchor" property to "TextBoxAnchor.TOP" to
# align the text in this text box with the top side of the shape.
# Set the "vertical_anchor" property to "TextBoxAnchor.MIDDLE" to
# align the text in this text box to the center of the shape.
# Set the "vertical_anchor" property to "TextBoxAnchor.BOTTOM" to
# align the text in this text box to the bottom of the shape.
shape.text_box.vertical_anchor = vertical_anchor

builder.move_to(shape.first_paragraph)
builder.write("Hello world!")

# The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(ARTIFACTS_DIR + "Shape.vertical_anchor.docx")
```

### See Also

* module [aspose.words.settings](../../)
* class [CompatibilityOptions](../)

