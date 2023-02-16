---
title: use_anti_aliasing property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value determining whether or not to use anti-aliasing for rendering."
type: docs
weight: 180
url: /python-net/aspose.words.saving/saveoptions/use_anti_aliasing/
---

## SaveOptions.use_anti_aliasing property

Gets or sets a value determining whether or not to use anti-aliasing for rendering.

The default value is ``False``. When this value is set to ``True`` anti-aliasing is
used for rendering.


This property is used when the document is exported to the following formats:
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF). When the document is exported to the
[SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../../aspose.words/saveformat/#MHTML),
[SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB), [SaveFormat.AZW3](../../../aspose.words/saveformat/#AZW3)
or [SaveFormat.MOBI](../../../aspose.words/saveformat/#MOBI) formats this option is used for raster images.




### Examples

Shows how to improve the quality of a rendered document with SaveOptions.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")
builder = aw.DocumentBuilder(doc)

builder.font.size = 60
builder.writeln("Some text.")

options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

doc.save(ARTIFACTS_DIR + "Document.image_save_options.default.jpg", options)

options.use_anti_aliasing = True
options.use_high_quality_rendering = True

doc.save(ARTIFACTS_DIR + "Document.image_save_options.high_quality.jpg", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

