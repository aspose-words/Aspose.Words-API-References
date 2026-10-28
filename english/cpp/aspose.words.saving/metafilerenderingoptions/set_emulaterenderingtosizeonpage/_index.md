---
title: Aspose::Words::Saving::MetafileRenderingOptions::set_EmulateRenderingToSizeOnPage method
linktitle: set_EmulateRenderingToSizeOnPage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::set_EmulateRenderingToSizeOnPage method. Sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size in C++.'
type: docs
weight: 12334
url: /cpp/aspose.words.saving/metafilerenderingoptions/set_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::set_EmulateRenderingToSizeOnPage method


Sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size.

```cpp
void Aspose::Words::Saving::MetafileRenderingOptions::set_EmulateRenderingToSizeOnPage(bool value)
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
