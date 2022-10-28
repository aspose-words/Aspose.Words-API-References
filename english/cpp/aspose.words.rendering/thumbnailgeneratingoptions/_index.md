---
title: ThumbnailGeneratingOptions
second_title: Aspose.Words for C++ API Reference
description: Can be used to specify additional options when generating thumbnail for a document.
type: docs
weight: 53
url: /cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Can be used to specify additional options when generating thumbnail for a document.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Specifies whether to generate thumbnail from first page of the document or first image. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Size of generated thumbnail in pixels. Default is 600x900. |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Setter for [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Setter for [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |

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

