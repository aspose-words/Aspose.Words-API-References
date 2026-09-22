---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment metodu"
linktitle: "get_Alignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment metodu. C++'da yatay kuralın hizalamasını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing/horizontalruleformat/get_alignment/
---
## HorizontalRuleFormat::get_Alignment method


Yatay kuralın hizalamasını alır veya ayarlar.

```cpp
Aspose::Words::Drawing::HorizontalRuleAlignment Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment()
```

## Açıklamalar


Varsayılan değer [Left](../../horizontalrulealignment/).

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

* Enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
