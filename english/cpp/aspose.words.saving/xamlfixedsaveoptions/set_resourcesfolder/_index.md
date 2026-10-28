---
title: Aspose::Words::Saving::XamlFixedSaveOptions::set_ResourcesFolder method
linktitle: set_ResourcesFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XamlFixedSaveOptions::set_ResourcesFolder method. Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is null in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/xamlfixedsaveoptions/set_resourcesfolder/
---
## XamlFixedSaveOptions::set_ResourcesFolder method


Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is **null**.

```cpp
void Aspose::Words::Saving::XamlFixedSaveOptions::set_ResourcesFolder(const System::String & value)
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [ResourcesFolder](../get_resourcesfolder/) allows you to specify where the images will be saved and [ResourcesFolderAlias](../get_resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ResourcesFolder](../get_resourcesfolder/) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [ResourcesFolder](../get_resourcesfolder/) property
## See Also

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
