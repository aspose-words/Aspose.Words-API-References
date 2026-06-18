---
title: Dml3DEffectsRenderingMode enumeration
linktitle: Dml3DEffectsRenderingMode enumeration
articleTitle: Dml3DEffectsRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.Dml3DEffectsRenderingMode enumeration. Specifies how 3D shape effects are rendered."
type: docs
weight: 70
url: /python-net/aspose.words.saving/dml3deffectsrenderingmode/
---

## Dml3DEffectsRenderingMode enumeration

Specifies how 3D shape effects are rendered.


### Members

| Name | Description |
| --- | --- |
| BASIC | A lightweight and stable rendering, based on the internal engine,  but advanced effects such as lighting, materials and other additional effects  are not displayed when using this mode. Please see documentation for details. |
| ADVANCED | Rendering of an extended list of special effects including advanced 3D effects  such as bevels, lighting and materials. |

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

* module [aspose.words.saving](../)

