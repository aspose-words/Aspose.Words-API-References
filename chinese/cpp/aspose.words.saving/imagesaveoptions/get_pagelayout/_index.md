---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout 方法"
linktitle: "get_PageLayout"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout 方法。获取或设置在 C++ 中将多页渲染为单个输出时使用的布局。"
type: docs
weight: 9500
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


获取或设置在将多个页面渲染为单个输出时使用的布局。

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## 备注


使用 [MultiPageLayout](../../multipagelayout/) 的工厂方法之一来配置此属性。

对于 [Tiff](../../../aspose.words/saveformat/) ，默认值是 [TiffFrames](../../multipagelayout/tiffframes/)。对于其他格式，默认值是 [SinglePage](../../multipagelayout/singlepage/)。

此属性仅在保存为以下格式时生效：[Jpeg](../../../aspose.words/saveformat/)、[Gif](../../../aspose.words/saveformat/)、[Png](../../../aspose.words/saveformat/)、[Bmp](../../../aspose.words/saveformat/)、[Tiff](../../../aspose.words/saveformat/)、[WebP](../)。

## 示例



展示如何使用多页布局设置将文档保存为 JPG 图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// 设置网格布局：
// - 每行 3 列。
// - 页面之间的间距为 10pt（水平和垂直）。
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// 可选布局：
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// 自定义背景和边框。
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## 另见

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
