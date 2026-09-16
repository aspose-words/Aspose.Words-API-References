---
title: "Aspose::Words::Rendering::PageInfo class"
linktitle: "PageInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::PageInfo 类。表示特定文档页的相关信息。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


表示特定文档页的信息。欲了解更多，请访问 [Rendering](https://docs.aspose.com/words/cpp/rendering/) 文档文章。

```cpp
class PageInfo : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Colored](./get_colored/)() | 如果页面包含彩色内容，则返回 **true**。 |
| [get_HeightInPoints](./get_heightinpoints/)() | 获取页面的高度（单位：点）。 |
| [get_Landscape](./get_landscape/)() const | 如果文档中为此页面指定的方向为横向，则返回 **true**。 |
| [get_PaperSize](./get_papersize/)() | 获取纸张尺寸（枚举）。 |
| [get_PaperTray](./get_papertray/)() const | 获取文档中指定的此页面的纸盒（托盘）。该值取决于实现（打印机）具体情况。 |
| [get_SizeInPoints](./get_sizeinpoints/)() const | 获取页面尺寸（以点为单位）。 |
| [get_WidthInPoints](./get_widthinpoints/)() | 获取页面宽度（以点为单位）。 |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | 根据指定的缩放因子和分辨率计算页面尺寸（以像素为单位）。 |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | 根据指定的缩放因子和分辨率计算页面尺寸（以像素为单位）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


此对象返回的页面宽度和高度表示页面的“最终”尺寸，例如它们已经旋转到正确的方向。

## 另见

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
