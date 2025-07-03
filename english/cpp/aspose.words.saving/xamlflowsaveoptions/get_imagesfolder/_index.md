---
title: Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder method
linktitle: get_ImagesFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder method. Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [ImagesFolder](./) allows you to specify where the images will be saved and [ImagesFolderAlias](../get_imagesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ImagesFolder](./) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [ImagesFolder](./) property or provide custom streams via the [ImageSavingCallback](../get_imagesavingcallback/) event handler.

## See Also

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
