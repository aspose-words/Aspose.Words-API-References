---
title: Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method
linktitle: get_EmulateRasterOperations
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method. Gets or sets a value determining whether or not the raster operations should be emulated in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Gets or sets a value determining whether or not the raster operations should be emulated.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Remarks


Specific raster operations could be used in metafiles. They can not be rendered directly to vector graphics. Emulating raster operations requires partial rasterization of the resulting vector graphics which may affect the metafile rendering performance.

When this value is set to **true**, Aspose.Words emulates the raster operations. The resulting output maybe partially rasterized and performance might be slower.

When this value is set to **false**, Aspose.Words does not emulate the raster operations. When [Aspose.Words](../../../aspose.words/) encounters a raster operation in a metafile it fallbacks to rendering the metafile into a bitmap by using the operating system.

This option is used only when metafile is rendered as vector graphics.

The default value is **true**. 
## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
