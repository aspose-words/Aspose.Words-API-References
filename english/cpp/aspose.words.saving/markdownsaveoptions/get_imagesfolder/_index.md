---
title: get_ImagesFolder
second_title: Aspose.Words for C++ API Reference
description: Specifies the physical folder where images are saved when exporting a document to the Markdown format. Default is an empty string.
type: docs
weight: 53
url: /cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Specifies the physical folder where images are saved when exporting a document to the [Markdown](../../../aspose.words/saveformat/) format. Default is an empty string.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in [Markdown](../../../aspose.words/saveformat/) format, Aspose.Words needs to save all images embedded in the document as standalone files. [ImagesFolder](./) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [ImagesFolder](./) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [ImagesFolder](./) property.

If the folder specified by [ImagesFolder](./) doesn't exist, it will be created automatically. 
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
