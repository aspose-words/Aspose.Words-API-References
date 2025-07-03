---
title: Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias method
linktitle: get_ImagesFolderAlias
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias method. Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string in C++.'
type: docs
weight: 5500
url: /cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in [Markdown](../../../aspose.words/saveformat/) format, Aspose.Words needs to save all images embedded in the document as standalone files. [ImagesFolder](../get_imagesfolder/) allows you to specify where the images will be saved and [ImagesFolderAlias](./) allows to specify how the image URIs will be constructed.

If [ImagesFolderAlias](./) is not an empty string, then the image URI written to Markdown will be *ImagesFolderAlias + <image file name>*.

If [ImagesFolderAlias](./) is an empty string, then the image URI written to Markdown will be *ImagesFolder + <image file name>*.

If [ImagesFolderAlias](./) is set to '.' (dot), then the image file name will be written to Markdown without path regardless of other options.

## Examples



Shows how to specifies the name of the folder used to construct image URIs. 
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Use the "ImagesFolder" property to assign a folder in the local file system into which
// Aspose.Words will save all the document's linked images.
saveOptions->set_ImagesFolder(imagesFolder);
// Use the "ImagesFolderAlias" property to use this folder
// when constructing image URIs instead of the images folder's name.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
