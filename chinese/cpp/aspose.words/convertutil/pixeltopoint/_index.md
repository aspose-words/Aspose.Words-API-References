---
title: "Aspose::Words::ConvertUtil::PixelToPoint method"
linktitle: "PixelToPoint"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConvertUtil::PixelToPoint 方法。将像素在 96 dpi 下转换为点（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/convertutil/pixeltopoint/
---
## ConvertUtil::PixelToPoint(double) method


在 96 dpi 下将像素转换为点。

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 像素 | double | 要转换的值。 |

## 示例



展示如何以像素指定页面属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 节的 "Page Setup" 定义页面边距的大小（单位为点）。
// 我们还可以使用 "ConvertUtil" 类来使用不同的计量单位，
// 例如在定义边界时使用像素。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// 一个像素等于 0.75 点。
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// 使用的默认 DPI 值为 96。
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// 添加内容以演示新的页边距。
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## 另见

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PixelToPoint(double, double) method


在指定的像素分辨率下将像素转换为点。

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels, double resolution)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 像素 | double | 要转换的值。 |
| 分辨率 | double | 该 dpi（每英寸点数）分辨率。 |

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
