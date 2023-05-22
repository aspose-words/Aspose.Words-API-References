---
title: RtfSaveOptions.export_compact_size property
linktitle: export_compact_size property
articleTitle: export_compact_size property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_compact_size property. Allows to make output RTF documents smaller in size, but if they contain  RTL (right-to-left) text, it will not be displayed correctly."
type: docs
weight: 20
url: /python-net/aspose.words.saving/rtfsaveoptions/export_compact_size/
---

## RtfSaveOptions.export_compact_size property

Allows to make output RTF documents smaller in size, but if they contain 
RTL (right-to-left) text, it will not be displayed correctly.

Default value is ``False``.


If the document that you want to convert to RTF using Aspose.Words does not contain
right-to-left text in languages like Arabic, then you can set this option to ``True``
to reduce the size of the resulting RTF.




### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Create an "RtfSaveOptions" object to pass to the document's "save" method to modify how we save it to an RTF.
options = aw.saving.RtfSaveOptions()

self.assertEqual(aw.SaveFormat.RTF, options.save_format)

# Set the "export_compact_size" property to "True" to
# reduce the saved document's size at the cost of right-to-left text compatibility.
options.export_compact_size = True

# Set the "export_images_for_old_readers" property to "True" to use extra keywords to ensure that our document is
# compatible with pre-Microsoft Word 97 readers and WordPad.
# Set the "export_images_for_old_readers" property to "False" to reduce the size of the document,
# but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options.export_images_for_old_readers = export_images_for_old_readers

doc.save(ARTIFACTS_DIR + "RtfSaveOptions.export_images.rtf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

