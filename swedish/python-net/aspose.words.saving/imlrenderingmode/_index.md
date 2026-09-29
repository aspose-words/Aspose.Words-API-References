---
title: ImlRenderingMode enumeration
linktitle: ImlRenderingMode enumeration
articleTitle: ImlRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImlRenderingMode enumeration. Specifies how ink (InkML) objects are rendered to fixed page formats."
type: docs
weight: 420
url: /sv/python-net/aspose.words.saving/imlrenderingmode/
---

## ImlRenderingMode enumeration

Specifies how ink (InkML) objects are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| FALLBACK | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| INK_ML | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode. |

### Examples

Shows how to render Ink object.

```python
doc = aw.Document(file_name=MY_DIR + 'Ink object.docx')
# Ställ in 'ImlRenderingMode.InkML' ignorerar reservform för bläck (InkML)-objektet och renderar InkML själv.
# Om renderingsresultatet är otillfredsställande,
# vänligen använd 'ImlRenderingMode.Fallback' för att få ett resultat som liknar tidigare versioner.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
save_options.iml_rendering_mode = aw.saving.ImlRenderingMode.INK_ML
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.RenderInkObject.jpeg', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

