---
title: Aspose::Words::Drawing::Shape::get_Adjustments method
linktitle: get_Adjustments
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::get_Adjustments method. Provides access to the adjustment raw values of a shape. For a shape that does not contain any adjustment raw values, it returns an empty collection in C++.'
type: docs
weight: 3834
url: /cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


Provides access to the adjustment raw values of a shape. For a shape that does not contain any adjustment raw values, it returns an empty collection.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
```


## Examples



Shows how to work with adjustment raw values. 
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

## See Also

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
