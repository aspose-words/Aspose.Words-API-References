---
title: SaveOptions.iml_rendering_mode property
linktitle: iml_rendering_mode property
articleTitle: iml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.iml_rendering_mode property. Gets or sets a value determining how ink (InkML) objects are rendered."
type: docs
weight: 70
url: /python-net/aspose.words.saving/saveoptions/iml_rendering_mode/
---

## SaveOptions.iml_rendering_mode property

Gets or sets a value determining how ink (InkML) objects are rendered.


```python
@property
def iml_rendering_mode(self) -> aspose.words.saving.ImlRenderingMode:
    ...

@iml_rendering_mode.setter
def iml_rendering_mode(self, value: aspose.words.saving.ImlRenderingMode):
    ...

```

### Remarks

The default value is [ImlRenderingMode.INK_ML](../../imlrenderingmode/#INK_ML).
This property is used when the document is exported to fixed page formats.




### Examples

Shows how to render Ink object.

```python
doc = aw.Document(MY_DIR + "Ink object.docx")

# Set 'ImlRenderingMode.INK_ML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
# If the rendering result is unsatisfactory,
# please use 'ImlRenderingMode.FALLBACK' to get a result similar to previous versions.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
save_options.iml_rendering_mode = aw.saving.ImlRenderingMode.INK_ML

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.render_ink_object.jpeg", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

