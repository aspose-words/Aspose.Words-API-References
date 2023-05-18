---
title: Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method
linktitle: get_UseGdiRasterOperationsEmulation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method. Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Remarks


Windows GDI+ library could be used to emulate raster operations. It provides support for all raster operation comparing to Aspose.Words own emulation but performance may be slower in some cases.

When this value is set to **true**, Aspose.Words uses GDI+ for raster operations emulation.

When this value is set to **false**, Aspose.Words uses its own implementation of raster operations emulation.

This option is used only when metafile is rendered as vector graphics.

The default value is **false**. 
## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
