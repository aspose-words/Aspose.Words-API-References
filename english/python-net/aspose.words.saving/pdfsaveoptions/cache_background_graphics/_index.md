---
title: PdfSaveOptions.cache_background_graphics property
linktitle: cache_background_graphics property
articleTitle: cache_background_graphics property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.cache_background_graphics property. Gets or sets a value determining whether or not to cache graphics placed in document's background."
type: docs
weight: 30
url: /python-net/aspose.words.saving/pdfsaveoptions/cache_background_graphics/
---

## PdfSaveOptions.cache_background_graphics property

Gets or sets a value determining whether or not to cache graphics placed in document's background.

Default value is ``True`` and background graphics are written to the PDF document as an xObject.

When the value is ``False`` background graphics are not cached.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

Document background graphic is various shapes, charts, images placed in the footer or header,
well as background and border of a page.




### Examples

Shows how to cache graphics placed in document's background.

```python
doc = aw.Document(MY_DIR + "Background images.docx")

save_options = aw.saving.PdfSaveOptions()
save_options.cache_background_graphics = True

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.CacheBackgroundGraphics.pdf", save_options)

aspose_to_pdf_size = os.stat(ARTIFACTS_DIR + "PdfSaveOptions.CacheBackgroundGraphics.pdf").st_size
word_to_pdf_size = os.stat(MY_DIR + "Background images (word to pdf).pdf").st_size

self.assertLess(aspose_to_pdf_size, word_to_pdf_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

