---
title: Aspose::Words::Saving::PdfSaveOptions::set_PreblendImages method
linktitle: set_PreblendImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::set_PreblendImages method. Sets a value determining whether or not to preblend transparent images with black background color in C++.'
type: docs
weight: 59000
url: /cpp/aspose.words.saving/pdfsaveoptions/set_preblendimages/
---
## PdfSaveOptions::set_PreblendImages method


Sets a value determining whether or not to preblend transparent images with black background color.

```cpp
void Aspose::Words::Saving::PdfSaveOptions::set_PreblendImages(bool value)
```

## Remarks


Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is **false**.
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
