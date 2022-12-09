---
title: get_ThumbnailSize
second_title: Aspose.Words for C++ API Reference
description: Size of generated thumbnail in pixels. Default is 600x900.
type: docs
weight: 40
url: /cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


Size of generated thumbnail in pixels. Default is 600x900.

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
```


## Examples



Shows how to update a document's thumbnail. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(ImageDir + u"Logo.jpg");

// There are two ways of setting a thumbnail image when saving a document to .epub.
// 1 -  Use the document's first page:
doc->UpdateThumbnail();
doc->Save(ArtifactsDir + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Use the first image found in the document:
auto options = MakeObject<ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(ArtifactsDir + u"Document.UpdateThumbnail.FirstImage.epub");
```

## See Also

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words](../../../)
