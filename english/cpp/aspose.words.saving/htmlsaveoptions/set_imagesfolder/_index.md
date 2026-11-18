---
title: Aspose::Words::Saving::HtmlSaveOptions::set_ImagesFolder method
linktitle: set_ImagesFolder
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_ImagesFolder method. Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string in C++.'
type: docs
weight: 85000
url: /cpp/aspose.words.saving/htmlsaveoptions/set_imagesfolder/
---
## HtmlSaveOptions::set_ImagesFolder method


Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_ImagesFolder(const System::String & value)
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [ImagesFolder](../get_imagesfolder/) allows you to specify where the images will be saved and [ImagesFolderAlias](../get_imagesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ImagesFolder](../get_imagesfolder/) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [ImagesFolder](../get_imagesfolder/) property or provide custom streams via the [ImageSavingCallback](../get_imagesavingcallback/) event handler.

If the folder specified by [ImagesFolder](../get_imagesfolder/) doesn't exist, it will be created automatically.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.
## Examples


Shows how to specify the folder for storing linked images after saving to .html.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
