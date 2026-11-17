---
title: Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages method
linktitle: get_PreblendImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages method. Gets or sets a value determining whether or not to preblend transparent images with black background color in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


Gets or sets a value determining whether or not to preblend transparent images with black background color.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## Remarks


Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is **false**. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
