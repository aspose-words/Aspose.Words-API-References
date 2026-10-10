---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment 方法"
linktitle: "get_Alignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment 方法。获取或设置水平线在 C++ 中的对齐方式。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/horizontalruleformat/get_alignment/
---
## HorizontalRuleFormat::get_Alignment method


获取或设置水平线的对齐方式。

```cpp
Aspose::Words::Drawing::HorizontalRuleAlignment Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment()
```

## 备注


默认值是 [Left](../../horizontalrulealignment/)。

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

* Enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
