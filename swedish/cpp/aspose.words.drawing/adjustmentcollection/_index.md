---
title: "Aspose::Words::Drawing::AdjustmentCollection-klass"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::AdjustmentCollection-klass. Representerar en skrivskyddad samling av Adjustment‑justeringsvärden som tillämpas på den angivna formen i C++."
type: docs
weight: 667
url: /sv/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Representerar en skrivskyddad samling av [Adjustment](../adjustment/) justeringsvärden som tillämpas på den angivna formen.

```cpp
class AdjustmentCollection : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar en justering på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
