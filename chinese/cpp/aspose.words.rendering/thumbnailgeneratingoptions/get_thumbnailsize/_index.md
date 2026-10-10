---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize 方法"
linktitle: "get_ThumbnailSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize 方法。生成的缩略图尺寸（像素）。默认值为 600x900，使用 C++。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


生成的缩略图的尺寸（像素）。默认是 600x900。

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
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

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
