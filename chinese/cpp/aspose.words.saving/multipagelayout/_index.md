---
title: "Aspose::Words::Saving::MultiPageLayout 类"
linktitle: "MultiPageLayout"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MultiPageLayout 类。定义了一种在 C++ 中将多个页面渲染到单个输出的布局。"
type: docs
weight: 14500
url: /zh/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


定义将多页渲染为单个输出的布局。

```cpp
class MultiPageLayout : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | 获取输出的背景颜色。默认是 **Empty**。 |
| [get_BorderColor](./get_bordercolor/)() | 获取页面边框的颜色。默认是 **Empty**。 |
| [get_BorderWidth](./get_borderwidth/)() const | 获取页面边框的宽度。默认是 0。 |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | 创建一种布局，使页面按从左到右、从上到下的顺序，在具有指定列数的网格中渲染。 |
| static [Horizontal](./horizontal/)(float) | 创建一种布局，使所有指定的页面水平并排、从左到右地渲染到单个输出中。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | 设置输出的背景颜色。默认是 **Empty**。 |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | 设置页面边框的颜色。默认是 **Empty**。 |
| [set_BorderWidth](./set_borderwidth/)(float) | 设置页面边框的宽度。默认是 0。 |
| static [SinglePage](./singlepage/)() | 创建一种布局，仅渲染指定页面中的第一页。 |
| static [TiffFrames](./tiffframes/)() | 创建一种布局，将每页渲染为多帧 TIFF 图像中的单独帧。仅适用于 TIFF 图像格式。 |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | 创建一种布局，使所有指定的页面垂直排列，一个接一个地渲染到单个输出中。 |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
