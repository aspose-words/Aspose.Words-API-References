---
title: Aspose::Words::Saving::ImageSaveOptions::get_PageLayout method
linktitle: get_PageLayout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_PageLayout method. Gets or sets the layout used when rendering multiple pages into a single output in C++.'
type: docs
weight: 9500
url: /cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Gets or sets the layout used when rendering multiple pages into a single output.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Remarks


Use one of the factory methods of [MultiPageLayout](../../multipagelayout/) to configure this property.

For [Tiff](../../../aspose.words/saveformat/) the default value is [TiffFrames](../../multipagelayout/tiffframes/). For other formats the default value is [SinglePage](../../multipagelayout/singlepage/).

This property has effect only when saving to the following formats: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)
## See Also

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
