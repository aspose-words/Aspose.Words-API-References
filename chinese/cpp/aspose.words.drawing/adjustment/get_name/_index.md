---
title: "Aspose::Words::Drawing::Adjustment::get_Name 方法"
linktitle: "get_Name"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Adjustment::get_Name 方法。获取 C++ 中调整的名称。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/adjustment/get_name/
---
## Adjustment::get_Name method


获取调整的名称。

```cpp
System::String Aspose::Words::Drawing::Adjustment::get_Name() const
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

* Class [Adjustment](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
