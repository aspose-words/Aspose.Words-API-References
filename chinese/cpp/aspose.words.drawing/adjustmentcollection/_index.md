---
title: "Aspose::Words::Drawing::AdjustmentCollection class"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::AdjustmentCollection 类。表示一个只读集合，其中包含应用于指定形状的 Adjustment 调整值（C++）。"
type: docs
weight: 667
url: /zh/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


表示一个只读集合，其中包含应用于指定形状的 [Adjustment](../adjustment/) 调整值。

```cpp
class AdjustmentCollection : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的调整值。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
