---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint 方法"
linktitle: "MillimeterToPoint"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint 方法。将毫米转换为 C++ 中的点。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


将毫米转换为点。

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 毫米 | double | 要转换的值。 |

## 示例



展示如何以毫米指定页面属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 节的 "Page Setup" 定义页面边距的大小（单位为点）。
// 我们也可以使用 "ConvertUtil" 类来使用更熟悉的计量单位，
// 例如在定义边界时使用毫米。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// 一厘米约等于 28.3 点。
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// 添加内容以演示新的页边距。
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## 另见

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
