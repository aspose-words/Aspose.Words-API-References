---
title: Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics method
linktitle: get_CacheBackgroundGraphics
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics method. Gets or sets a value determining whether or not to cache graphics placed in document''s background in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_cachebackgroundgraphics/
---
## PdfSaveOptions::get_CacheBackgroundGraphics method


Gets or sets a value determining whether or not to cache graphics placed in document's background.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics() const
```

## Remarks


Default value is **true** and background graphics are written to the PDF document as an xObject.

When the value is **false** background graphics are not cached.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

[Document](../../../aspose.words/document/) background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
