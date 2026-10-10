---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. 可用于在 C++ 中为文档生成缩略图时指定其他选项。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


可用于在为文档生成缩略图时指定其他选项。

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | 指定是从文档的首页还是第一张图像生成缩略图。 |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | 生成的缩略图的尺寸（像素）。默认是 600x900。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | 用于设置 [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/) 的 setter。 |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | 用于设置 [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/) 的 setter。 |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
