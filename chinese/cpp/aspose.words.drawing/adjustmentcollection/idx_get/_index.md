---
title: "Aspose::Words::Drawing::AdjustmentCollection::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::AdjustmentCollection::idx_get 方法。返回 C++ 中指定索引处的调整项。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing/adjustmentcollection/idx_get/
---
## AdjustmentCollection::idx_get method


返回指定索引处的调整值。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Adjustment> Aspose::Words::Drawing::AdjustmentCollection::idx_get(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 集合中的索引。 |

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

* Class [Adjustment](../../adjustment/)
* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
