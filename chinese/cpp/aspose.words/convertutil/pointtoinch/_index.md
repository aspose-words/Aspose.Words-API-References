---
title: "Aspose::Words::ConvertUtil::PointToInch method"
linktitle: "PointToInch"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConvertUtil::PointToInch 方法。将点转换为英寸（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


将点转换为英寸。

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 点 | double | 要转换的值。 |

## 示例



展示如何以英寸指定页面属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 节的 "Page Setup" 定义页面边距的大小（单位为点）。
// 我们也可以使用 "ConvertUtil" 类来使用更熟悉的计量单位，
// 例如在定义边界时使用英寸。
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// 一英寸等于 72 点。
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// 添加内容以演示新的页边距。
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## 另见

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
