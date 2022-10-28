---
title: always_compress_metafiles property
second_title: Aspose.Words for Python via .NET API Reference
description: "When ``False``, small metafiles are not compressed for performance reason"
type: docs
weight: 20
url: /python-net/aspose.words.saving/docsaveoptions/always_compress_metafiles/
---

## DocSaveOptions.always_compress_metafiles property

When ``False``, small metafiles are not compressed for performance reason.
Default value is ``True``, all metafiles are compressed regardless of its size.



### Examples

Shows how to change metafiles compression in a document while saving.

```python
# Open a document that contains a Microsoft Equation 3.0 formula.
doc = aw.Document(MY_DIR + "Microsoft equation object.docx")

# When we save a document, smaller metafiles are not compressed for performance reasons.
# We can set a flag in a SaveOptions object to compress every metafile when saving.
# Some editors such as LibreOffice cannot read uncompressed metafiles.
save_options = aw.saving.DocSaveOptions()
save_options.always_compress_metafiles = compress_all_metafiles

doc.save(ARTIFACTS_DIR + "DocSaveOptions.always_compress_metafiles.docx", save_options)

if compress_all_metafiles:
    self.assertLess(10000, os.path.getsize(ARTIFACTS_DIR + "DocSaveOptions.always_compress_metafiles.docx"))
else:
    self.assertGreater(30000, os.path.getsize(ARTIFACTS_DIR + "DocSaveOptions.always_compress_metafiles.docx"))
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

