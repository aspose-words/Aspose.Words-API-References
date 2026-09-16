---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize 方法"
linktitle: "get_ImageSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize 方法。获取或设置在 C++ 中生成图像的像素尺寸。"
type: docs
weight: 7500
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


获取或设置生成图像的大小（像素）。

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## 备注


此属性仅在保存为光栅图像格式时生效。

默认值为 (0 x 0)，这意味着生成图像的尺寸将根据图像的点大小、指定的分辨率和比例进行计算。

## 示例



展示如何将文档的每一页渲染为单独的 TIFF 图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // 将 "PageSet" 属性设置为起始页的页码，从
    // 该页开始渲染文档。
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // 以 2325x5325 像素、600 dpi 导出页面。
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## 另见

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
