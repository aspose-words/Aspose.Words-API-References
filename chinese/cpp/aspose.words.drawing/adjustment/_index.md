---
title: "Aspose::Words::Drawing::Adjustment 类"
linktitle: "Adjustment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Adjustment 类。表示在 C++ 中应用于指定形状的调整值。"
type: docs
weight: 334
url: /zh/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


表示应用于指定形状的调整值。

```cpp
class Adjustment : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Name](./get_name/)() const | 获取调整的名称。 |
| [get_Value](./get_value/)() const | 获取或设置调整的原始值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | 用于 [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/) 的设置器。 |
| static [Type](./type/)() |  |

## 示例



展示如何使用调整的原始值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rounded rectangle shape.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(1, adjustments->get_Count());

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(u"adj", adjustment->get_Name());
ASSERT_EQ(16667, adjustment->get_Value());

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
