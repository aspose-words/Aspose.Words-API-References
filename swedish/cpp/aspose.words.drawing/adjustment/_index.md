---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Adjustment class. Representerar justeringsvärden som tillämpas på den angivna formen i C++."
type: docs
weight: 334
url: /sv/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Representerar justeringsvärden som tillämpas på den angivna formen.

```cpp
class Adjustment : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Name](./get_name/)() const | Hämtar namnet på justeringen. |
| [get_Value](./get_value/)() const | Hämtar eller anger det råa värdet för justeringen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Sättare för [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
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
