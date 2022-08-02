---
title: save_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /python-net/aspose.words.saving/pclsaveoptions/save_format/
---

## PclSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.PCL](../../../aspose.words/saveformat/#PCL).



### Examples

Shows how to rasterize complex elements while saving a document to PCL.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

save_options = aw.saving.PclSaveOptions()
save_options.save_format = aw.SaveFormat.PCL
save_options.rasterize_transformed_elements = True

doc.save(ARTIFACTS_DIR + "PclSaveOptions.rasterize_elements.pcl", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PclSaveOptions](../)

