---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade 方法"
linktitle: "get_NoShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade 方法。指示水平线是否具有 3D 阴影。如果为 true，则水平线没有 3D 阴影，并在 C++ 中使用纯色。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


指示水平线是否具有 3D 阴影。如果 **true**，则水平线没有 3D 阴影，使用纯色。

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## 备注


默认值为 **false**。

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
