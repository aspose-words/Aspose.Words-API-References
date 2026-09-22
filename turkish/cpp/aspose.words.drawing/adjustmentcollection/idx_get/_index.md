---
title: "Aspose::Words::Drawing::AdjustmentCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::AdjustmentCollection::idx_get yöntemi. C++'da belirtilen indeksteki ayarlamayı döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing/adjustmentcollection/idx_get/
---
## AdjustmentCollection::idx_get method


Belirtilen indekste bir ayarlama döndürür.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Adjustment> Aspose::Words::Drawing::AdjustmentCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Koleksiyona bir indeks. |

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

* Class [Adjustment](../../adjustment/)
* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
