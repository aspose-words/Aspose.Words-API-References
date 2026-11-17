---
title: Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode method
linktitle: get_EmfPlusDualRenderingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode method. Gets or sets a value determining how EMF+ Dual metafiles should be rendered in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Gets or sets a value determining how EMF+ Dual metafiles should be rendered.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Remarks


EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is [EmfPlusWithFallback](../../emfplusdualrenderingmode/). 
## See Also

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
