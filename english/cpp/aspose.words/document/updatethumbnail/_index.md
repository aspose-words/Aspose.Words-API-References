---
title: Aspose::Words::Document::UpdateThumbnail method
linktitle: UpdateThumbnail
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::UpdateThumbnail method. Updates Thumbnail of the document using default options in C++.'
type: docs
weight: 100000
url: /cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Updates [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) of the document using default options.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
```


## Examples



Shows how to update a document's thumbnail. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// There are two ways of setting a thumbnail image when saving a document to .epub.
// 1 -  Use the document's first page:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Use the first image found in the document:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Updates [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) of the document according to the specified options.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | The generating options to use. |

## Examples



Shows how to update a document's thumbnail. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// There are two ways of setting a thumbnail image when saving a document to .epub.
// 1 -  Use the document's first page:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Use the first image found in the document:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## See Also

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
