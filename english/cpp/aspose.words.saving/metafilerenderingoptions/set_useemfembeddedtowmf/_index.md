---
title: Aspose::Words::Saving::MetafileRenderingOptions::set_UseEmfEmbeddedToWmf method
linktitle: set_UseEmfEmbeddedToWmf
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::set_UseEmfEmbeddedToWmf method. Sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.saving/metafilerenderingoptions/set_useemfembeddedtowmf/
---
## MetafileRenderingOptions::set_UseEmfEmbeddedToWmf method


Sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered.

```cpp
void Aspose::Words::Saving::MetafileRenderingOptions::set_UseEmfEmbeddedToWmf(bool value)
```

## Remarks


WMF metafiles could contain embedded EMF data. MS Word in most cases uses embedded EMF data. GDI+ always uses WMF data.

When this value is set to **true**, Aspose.Words uses embedded EMF data when rendering.

When this value is set to **false**, Aspose.Words uses WMF data when rendering.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, WMF data is always used.

The default value is **true**.
## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
