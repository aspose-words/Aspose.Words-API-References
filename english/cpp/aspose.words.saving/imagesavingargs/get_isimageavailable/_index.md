---
title: Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable method
linktitle: get_IsImageAvailable
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable method. Returns true if the current image is available for export in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Returns **true** if the current image is available for export.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Remarks


Some images in the document can be unavailable, for example, because the image is linked and the link is inaccessible or does not point to a valid image. In this case Aspose.Words exports an icon with a red cross. This property returns **true** if the original image is available; returns **false** if the original image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property is always **true**.

## See Also

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
