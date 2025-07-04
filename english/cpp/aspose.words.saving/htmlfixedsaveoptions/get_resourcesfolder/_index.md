---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder method
linktitle: get_ResourcesFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder method. Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is null in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## Remarks


Has effect only if [ExportEmbeddedImages](../get_exportembeddedimages/) property is **false**.

When you save a [Document](../../../aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [ResourcesFolder](./) allows you to specify where the images will be saved and [ResourcesFolderAlias](../get_resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ResourcesFolder](./) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [ResourcesFolder](./) property

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
