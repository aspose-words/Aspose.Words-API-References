---
title: "Aspose::Words::Drawing::AdjustmentCollection Klasse"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::AdjustmentCollection Klasse. Stellt eine schreibgeschützte Sammlung von Adjustment-Anpassungswerten dar, die auf die angegebene Form in C++ angewendet werden."
type: docs
weight: 667
url: /de/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Stellt eine schreibgeschützte Sammlung von [Adjustment](../adjustment/) Anpassungswerten dar, die auf die angegebene Form angewendet werden.

```cpp
class AdjustmentCollection : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt eine Anpassung am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
