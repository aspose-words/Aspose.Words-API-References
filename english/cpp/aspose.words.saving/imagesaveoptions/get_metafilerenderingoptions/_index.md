---
title: Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions method
linktitle: get_MetafileRenderingOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions method. Allows to specify how metafiles are treated in the rendered output in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Allows to specify how metafiles are treated in the rendered output.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Remarks


When [Vector](../../metafilerenderingmode/) is specified, Aspose.Words renders metafile to vector graphics using its own metafile rendering engine first and then renders vector graphics to the image.

When [Bitmap](../../metafilerenderingmode/) is specified, Aspose.Words renders metafile directly to the image using the GDI+ metafile rendering engine.

GDI+ metafile rendering engine works faster, supports almost all metafile features but on low resolutions may produce inconsistent result when compared to the rest of vector graphics (especially for text) on the page. Aspose.Words metafile rendering engine will produce more consistent result even on low resolutions but works slower and may inaccurately render complex metafiles.

The default value for [MetafileRenderingMode](../../metafilerenderingmode/) is [Bitmap](../../metafilerenderingmode/). 
## See Also

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
