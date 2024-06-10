---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
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
doc.save(ARTIFACTS_DIR + 'RtfSaveOptions.export_images.rtf', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

