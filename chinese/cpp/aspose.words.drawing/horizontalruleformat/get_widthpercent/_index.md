---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent 方法"
linktitle: "get_WidthPercent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent 方法。获取或设置指定水平线的长度，以窗口宽度的百分比表示，在 C++ 中。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


获取或设置指定水平线的长度，以窗口宽度的百分比表示。

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## 备注


有效值范围为 1 到 100（含）。

默认值为 100。

## 示例



展示如何插入水平线形状并自定义其格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

## 另见

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
