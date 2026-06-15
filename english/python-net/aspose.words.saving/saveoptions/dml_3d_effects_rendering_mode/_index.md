---
title: SaveOptions.dml_3d_effects_rendering_mode property
linktitle: dml_3d_effects_rendering_mode property
articleTitle: dml_3d_effects_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_3d_effects_rendering_mode property. Gets or sets a value determining how 3D effects are rendered."
type: docs
weight: 30
url: /python-net/aspose.words.saving/saveoptions/dml_3d_effects_rendering_mode/
---

## SaveOptions.dml_3d_effects_rendering_mode property

Gets or sets a value determining how 3D effects are rendered.


```python
@property
def dml_3d_effects_rendering_mode(self) -> aspose.words.saving.Dml3DEffectsRenderingMode:
    ...

@dml_3d_effects_rendering_mode.setter
def dml_3d_effects_rendering_mode(self, value: aspose.words.saving.Dml3DEffectsRenderingMode):
    ...

```

### Remarks

The default value is [Dml3DEffectsRenderingMode.BASIC](../../dml3deffectsrenderingmode/#BASIC).



### Examples

Shows how 3D effects are rendered.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape 3D effects.docx')
warning_callback = self.RenderCallback()
doc.warning_callback = warning_callback
save_options = aw.saving.PdfSaveOptions()
save_options.dml_3d_effects_rendering_mode = aw.saving.Dml3DEffectsRenderingMode.ADVANCED
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

