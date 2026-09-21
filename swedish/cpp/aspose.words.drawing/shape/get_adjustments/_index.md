---
title: "Aspose::Words::Drawing::Shape::get_Adjustments metod"
linktitle: "get_Adjustments"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Shape::get_Adjustments metod. Tillhandahåller åtkomst till de råa justeringsvärdena för en form. För en form som inte innehåller några justeringsvärden returneras en tom samling i C++."
type: docs
weight: 3834
url: /sv/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


Tillhandahåller åtkomst till justeringsråvärdena för en form. För en form som inte innehåller några justeringsråvärden returneras en tom samling.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
```


## Exempel



Visar hur man arbetar med råa justeringsvärden.
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

## Se även

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
