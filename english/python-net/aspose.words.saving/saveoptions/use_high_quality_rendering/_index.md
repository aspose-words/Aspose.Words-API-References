﻿---
title: SaveOptions.use_high_quality_rendering property
linktitle: use_high_quality_rendering property
articleTitle: use_high_quality_rendering property
second_title: Aspose.Words for Python
description: "SaveOptions.use_high_quality_rendering property. Gets or sets a value determining whether or not to use high quality (i.e"
type: docs
weight: 190
url: /python-net/aspose.words.saving/saveoptions/use_high_quality_rendering/
---

## SaveOptions.use_high_quality_rendering property

Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.


```python
@property
def use_high_quality_rendering(self) -> bool:
    ...

@use_high_quality_rendering.setter
def use_high_quality_rendering(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.
This property is used when the document is exported to image formats:
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF).




### Examples

Shows how to improve the quality of a rendered document with SaveOptions.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 60
builder.writeln('Some text.')
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageSaveOptions.Default.jpg', save_options=options)
options.use_anti_aliasing = True
options.use_high_quality_rendering = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageSaveOptions.HighQuality.jpg', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

