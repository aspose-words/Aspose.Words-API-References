---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment enum"
linktitle: "HorizontalRuleAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment enum. Belirtilen yatay kural için hizalamayı C++'da temsil eder."
type: docs
weight: 27000
url: /tr/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Belirtilen yatay kural için hizalamayı temsil eder.

```cpp
enum class HorizontalRuleAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Sol | 0 | Sola hizalı. |
| Orta | 1 | Ortaya hizalı. |
| Sağ | 2 | Sağa hizalı. |


## Örnekler



Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
