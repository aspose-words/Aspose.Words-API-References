---
title: UpdateThumbnail
second_title: Aspose.Words for C++ API Reference
description: Updates Thumbnail of the document using default options.
type: docs
weight: 1236
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
