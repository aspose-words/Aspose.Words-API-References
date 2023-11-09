---
title: RtfSaveOptions.export_images_for_old_readers property
linktitle: export_images_for_old_readers property
articleTitle: export_images_for_old_readers property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_images_for_old_readers property. Specifies whether the keywords for old readers are written to RTF or not"
type: docs
weight: 30
url: /python-net/aspose.words.saving/rtfsaveoptions/export_images_for_old_readers/
---

## RtfSaveOptions.export_images_for_old_readers property

Specifies whether the keywords for "old readers" are written to RTF or not.
This can significantly affect the size of the RTF document.

Default value is ``True``.



```python
@property
def export_images_for_old_readers(self) -> bool:
    ...

@export_images_for_old_readers.setter
def export_images_for_old_readers(self, value: bool):
    ...

```

### Remarks

"Old readers" are pre-Microsoft Word 97 applications and also WordPad.
When this option is ``True`` Aspose.Words writes additional RTF keywords.
These keywords allow the document to be displayed correctly when opened in an 
"old reader" application, but can significantly increase the size of the document.

If you set this option to ``False``, then only images in WMF, EMF and BMP formats
will be displayed in "old readers".




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

