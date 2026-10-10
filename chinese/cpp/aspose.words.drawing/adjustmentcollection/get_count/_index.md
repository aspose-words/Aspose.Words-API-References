---
title: "Aspose::Words::Drawing::AdjustmentCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::AdjustmentCollection::get_Count 方法。获取集合中包含的元素数量（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/adjustmentcollection/get_count/
---
## AdjustmentCollection::get_Count method


获取集合中包含的元素数量。

```cpp
int32_t Aspose::Words::Drawing::AdjustmentCollection::get_Count()
```


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

* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
