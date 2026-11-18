---
title: Aspose::Words::Saving::XamlFlowSaveOptions::set_ImagesFolderAlias method
linktitle: set_ImagesFolderAlias
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XamlFlowSaveOptions::set_ImagesFolderAlias method. Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/xamlflowsaveoptions/set_imagesfolderalias/
---
## XamlFlowSaveOptions::set_ImagesFolderAlias method


Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string.

```cpp
void Aspose::Words::Saving::XamlFlowSaveOptions::set_ImagesFolderAlias(const System::String & value)
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [ImagesFolder](../get_imagesfolder/) allows you to specify where the images will be saved and [ImagesFolderAlias](../get_imagesfolderalias/) allows to specify how the image URIs will be constructed.

If [ImagesFolderAlias](../get_imagesfolderalias/) is not an empty string, then the image URI written to XAML will be ImagesFolderAlias + <image file name>.

If [ImagesFolderAlias](../get_imagesfolderalias/) is an empty string, then the image URI written to XAML will be ImagesFolder + <image file name>.

If [ImagesFolderAlias](../get_imagesfolderalias/) is set to '.' (dot), then the image file name will be written to XAML without path regardless of other options.
## See Also

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
