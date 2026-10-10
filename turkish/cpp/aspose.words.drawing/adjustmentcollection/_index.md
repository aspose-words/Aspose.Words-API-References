---
title: "Aspose::Words::Drawing::AdjustmentCollection sınıfı"
linktitle: "AdjustmentCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::AdjustmentCollection sınıfı. Belirtilen şekle C++'da uygulanan Adjustment ayar değerlerinin yalnızca okunabilir bir koleksiyonunu temsil eder."
type: docs
weight: 667
url: /tr/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Belirtilen şekle uygulanan [Adjustment](../adjustment/) ayar değerlerinin yalnızca okunabilir bir koleksiyonunu temsil eder.

```cpp
class AdjustmentCollection : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indekste bir ayarlama döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
