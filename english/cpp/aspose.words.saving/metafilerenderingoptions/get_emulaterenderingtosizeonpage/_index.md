---
title: Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method
linktitle: get_EmulateRenderingToSizeOnPage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method. Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size in C++.'
type: docs
weight: 4334
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Remarks


When metafiles are displayed in MS Word, some graphics may be scaled according to the actual metafile size in pixels. I.e. even zooming may affect the metafile display.

When this value is set to **true**, Aspose.Words emulates rendering according to the metafile size on page. The size in pixels is calculated from the metafile size on the page and the specified [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/).

When this value is set to **false**, Aspose.Words emulates metafile rendering to its default size in pixels.

This option is used only when metafile is rendered as vector graphics.

The default value is **true**. 
## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
