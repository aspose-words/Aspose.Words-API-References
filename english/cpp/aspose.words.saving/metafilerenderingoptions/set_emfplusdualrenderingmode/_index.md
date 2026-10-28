---
title: Aspose::Words::Saving::MetafileRenderingOptions::set_EmfPlusDualRenderingMode method
linktitle: set_EmfPlusDualRenderingMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MetafileRenderingOptions::set_EmfPlusDualRenderingMode method. Sets a value determining how EMF+ Dual metafiles should be rendered in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/metafilerenderingoptions/set_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::set_EmfPlusDualRenderingMode method


Sets a value determining how EMF+ Dual metafiles should be rendered.

```cpp
void Aspose::Words::Saving::MetafileRenderingOptions::set_EmfPlusDualRenderingMode(Aspose::Words::Saving::EmfPlusDualRenderingMode value)
```

## Remarks


EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part. Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered to bitmap, EMF+ part is always used.

The default value is [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
