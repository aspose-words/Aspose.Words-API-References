---
title: "Aspose::Words::Drawing::AdjustmentCollection::get_Count Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::AdjustmentCollection::get_Count Methode. Ermittelt die Anzahl der in der Sammlung enthaltenen Elemente in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing/adjustmentcollection/get_count/
---
## AdjustmentCollection::get_Count method


Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück.

```cpp
int32_t Aspose::Words::Drawing::AdjustmentCollection::get_Count()
```


## Beispiele



Zeigt, wie mit rohen Anpassungswerten gearbeitet wird.
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

## Siehe auch

* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
