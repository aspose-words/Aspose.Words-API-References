---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Adjustment class. Stellt Anpassungswerte dar, die auf die angegebene Form in C++ angewendet werden."
type: docs
weight: 334
url: /de/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Stellt Anpassungswerte dar, die auf die angegebene Form angewendet werden.

```cpp
class Adjustment : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Name](./get_name/)() const | Liefert den Namen der Anpassung. |
| [get_Value](./get_value/)() const | Liefert oder setzt den Rohwert der Anpassung. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Setter für [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
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
