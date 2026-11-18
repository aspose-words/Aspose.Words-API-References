---
title: Aspose::Words::Saving::ImageSavingArgs::set_ImageStream method
linktitle: set_ImageStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSavingArgs::set_ImageStream method. Allows to specify the stream where the image will be saved to in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/imagesavingargs/set_imagestream/
---
## ImageSavingArgs::set_ImageStream(const System::SharedPtr\<System::IO::Stream\> \&) method


Allows to specify the stream where the image will be saved to.

```cpp
void Aspose::Words::Saving::ImageSavingArgs::set_ImageStream(const System::SharedPtr<System::IO::Stream> & value)
```

## Remarks


This property allows you to save images to streams instead of files during HTML.

The default value is **null**. When this property is **null**, the image will be saved to a file specified in the [ImageFileName](../get_imagefilename/) property.

Using [IImageSavingCallback](../../iimagesavingcallback/) you cannot substitute one image with another. It is intended only for control over location where to save images.
## See Also

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## ImageSavingArgs::set_ImageStream(std::basic_ostream\<CharType, Traits\> \&) method


Allows to specify the stream where the image will be saved to.

```cpp
template<typename CharType,typename Traits> void Aspose::Words::Saving::ImageSavingArgs::set_ImageStream(std::basic_ostream<CharType, Traits> & value)
```

## Remarks


This property allows you to save images to streams instead of files during HTML.

The default value is **null**. When this property is **null**, the image will be saved to a file specified in the [ImageFileName](../get_imagefilename/) property.

Using [IImageSavingCallback](../../iimagesavingcallback/) you cannot substitute one image with another. It is intended only for control over location where to save images.
## See Also

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
