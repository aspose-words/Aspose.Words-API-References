---
title: Aspose::Words::Saving::ImageSavingArgs::get_ImageStream method
linktitle: get_ImageStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSavingArgs::get_ImageStream method. Allows to specify the stream where the image will be saved to in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/imagesavingargs/get_imagestream/
---
## ImageSavingArgs::get_ImageStream method


Allows to specify the stream where the image will be saved to.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ImageSavingArgs::get_ImageStream() const
```

## Remarks


This property allows you to save images to streams instead of files during HTML.

The default value is **null**. When this property is **null**, the image will be saved to a file specified in the [ImageFileName](../get_imagefilename/) property.

Using [IImageSavingCallback](../../iimagesavingcallback/) you cannot substitute one image with another. It is intended only for control over location where to save images.

## See Also

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
