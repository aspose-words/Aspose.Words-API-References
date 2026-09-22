---
title: "Aspose::Words::Drawing::Shape::get_Adjustments method"
linktitle: "get_Adjustments"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_Adjustments method. Bir şeklin ayar ham değerleri yoksa, C++'da boş bir koleksiyon döndürür."
type: docs
weight: 3834
url: /tr/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


Bir şeklin ayar ham değerlerine erişim sağlar. Herhangi bir ayar ham değeri içermeyen bir şekil için boş bir koleksiyon döndürür.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
```


## Örnekler



Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.
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

## Ayrıca Bakınız

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
