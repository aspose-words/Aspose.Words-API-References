---
title: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution 方法"
linktitle: "set_Resolution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution 方法。设置生成图像的水平和垂直分辨率，单位为每英寸点数（DPI），在 C++ 中。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


设置生成图像的水平和垂直分辨率，单位为每英寸点数（dpi）。

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## 备注


此属性仅在保存为光栅图像格式时生效。

## 示例



展示如何在将文档渲染为 PNG 时指定分辨率。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// 将 "Resolution" 属性设置为 "72"，以 72dpi 渲染文档。
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// 将 "Resolution" 属性设置为 "300"，以 300dpi 渲染文档。
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## 另见

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
