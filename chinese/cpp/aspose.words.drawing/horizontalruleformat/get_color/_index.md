---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color 方法"
linktitle: "get_Color"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color 方法。获取或设置填充水平线的画笔颜色（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/horizontalruleformat/get_color/
---
## HorizontalRuleFormat::get_Color method


获取或设置填充水平线的画笔颜色。

```cpp
System::Drawing::Color Aspose::Words::Drawing::HorizontalRuleFormat::get_Color()
```

## 备注


这是指向 [Color](../../fill/get_color/) 属性的快捷方式。

默认值是 **Gray**。

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
