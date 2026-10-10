---
title: "Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution 方法"
linktitle: "get_HorizontalResolution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution 方法。获取或设置生成图像的水平分辨率，单位为每英寸点数（DPI），在 C++ 中。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_horizontalresolution/
---
## ImageSaveOptions::get_HorizontalResolution method


获取或设置生成图像的水平分辨率（单位为每英寸点数）。

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution() const
```

## 备注


此属性仅在保存为光栅图像格式时生效，并影响输出的像素尺寸。

默认值为 96。

## 示例



展示在 Aspose.Words 将文档转换为图像的同时如何编辑该图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象给
// 在保存操作渲染图像的同时编辑该图像。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// 我们可以调整这些属性以改变图像的亮度和对比度。
// 两者均采用 0-1 的比例，默认值为 0.5。
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// 我们可以使用这些属性调整水平和垂直分辨率。
// 这将影响图像的尺寸。
// 这些属性的默认值为 96.0，对应分辨率为 96dpi。
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// 我们可以使用此属性对图像进行缩放。默认值为 1.0，表示 100% 的缩放比例。
// 我们可以使用此属性抵消因更改分辨率而导致的图像尺寸变化。
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## 另见

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
