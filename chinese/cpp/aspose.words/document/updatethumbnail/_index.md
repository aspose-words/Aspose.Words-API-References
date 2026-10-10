---
title: "Aspose::Words::Document::UpdateThumbnail 方法"
linktitle: "UpdateThumbnail"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UpdateThumbnail 方法。使用默认选项在 C++ 中更新文档的缩略图。"
type: docs
weight: 100000
url: /zh/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


使用默认选项更新文档的 [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/)。

```cpp
void Aspose::Words::Document::UpdateThumbnail()
```


## 示例



展示如何更新文档的缩略图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 在将文档保存为 .epub 时，有两种设置缩略图的方法。
// 1 - 使用文档的首页：
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 - 使用文档中找到的第一张图片：
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


根据指定的选项更新文档的[Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/)。

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| options | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | 要使用的生成选项。 |

## 示例



展示如何更新文档的缩略图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 在将文档保存为 .epub 时，有两种设置缩略图的方法。
// 1 - 使用文档的首页：
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 - 使用文档中找到的第一张图片：
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## 另见

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
