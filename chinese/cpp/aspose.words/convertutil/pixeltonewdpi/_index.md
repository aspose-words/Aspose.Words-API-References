---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi 方法"
linktitle: "PixelToNewDpi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi 方法。将像素从一种分辨率转换为另一种分辨率（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


将像素从一种分辨率转换为另一种分辨率。

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 像素 | double | 要转换的值。 |
| oldDpi | double | 当前的 dpi（每英寸点数）分辨率。 |
| newDpi | double | 新的 dpi（每英寸点数）分辨率。 |

## 示例



展示如何使用默认和自定义分辨率将点转换为像素。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 根据自定义 DPI，定义此部分顶部边距的像素大小。
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// 在默认 DPI 为 96 时，一个像素等于 0.75 点。
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// 设置新的 DPI 并相应调整顶部边距值。
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## 另见

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
