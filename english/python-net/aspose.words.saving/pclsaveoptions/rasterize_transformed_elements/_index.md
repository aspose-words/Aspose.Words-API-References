---
title: PclSaveOptions.rasterize_transformed_elements property
linktitle: rasterize_transformed_elements property
articleTitle: rasterize_transformed_elements property
second_title: Aspose.Words for Python
description: "PclSaveOptions.rasterize_transformed_elements property. Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document"
type: docs
weight: 30
url: /python-net/aspose.words.saving/pclsaveoptions/rasterize_transformed_elements/
---

## PclSaveOptions.rasterize_transformed_elements property

Gets or sets a value determining whether or not complex transformed elements
should be rasterized before saving to PCL document.
Default is ``True``.


PCL doesn't support some kind of transformations that are used by Aspose Words.
E.g. rotated, skewed images and texture brushes. To properly render such elements
rasterization process is used, i.e. saving to image and clipping.
This process can take additional time and memory.
If flag is set to ``False``, some content in output may be different
as compared with the source document.



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

