---
title: "Aspose::Words::Drawing::Shape::get_Adjustments 方法"
linktitle: "get_Adjustments"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Shape::get_Adjustments 方法。提供对形状调整原始值的访问。对于不包含任何调整原始值的形状，在 C++ 中返回空集合。"
type: docs
weight: 3834
url: /zh/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


提供对形状的调整原始值的访问。对于不包含任何调整原始值的形状，它返回空集合。

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
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

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
