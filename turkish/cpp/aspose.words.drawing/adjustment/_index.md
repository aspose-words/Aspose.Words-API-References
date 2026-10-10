---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Adjustment class. C++'ta belirtilen şekle uygulanan ayar değerlerini temsil eder."
type: docs
weight: 334
url: /tr/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Belirtilen şekle uygulanan ayar değerlerini temsil eder.

```cpp
class Adjustment : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Name](./get_name/)() const | Ayarlamanın adını alır. |
| [get_Value](./get_value/)() const | Ayarlamanın ham değerini alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/) için ayarlayıcı. |
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
