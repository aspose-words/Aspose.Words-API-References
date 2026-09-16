---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor 方法"
linktitle: "get_PaperColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor 方法。获取或设置生成图像的背景（纸张）颜色。默认值在 C++ 中为 White。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


获取或设置生成图像的背景（纸张）颜色。默认值为 **White**。

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## 备注


在渲染指定了自身背景颜色的文档页面时，文档的背景颜色将覆盖此属性指定的颜色。

## 示例



将 Word 文档的页面渲染为具有透明或彩色背景的图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// 将 "PaperColor" 属性设置为透明颜色，以应用透明
// 背景到文档，在将其渲染为图像时。
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// 将 "PaperColor" 属性设置为不透明颜色，以应用该颜色
// 作为文档的背景，在我们将其渲染为图像时。
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## 另见

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
