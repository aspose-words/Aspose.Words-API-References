---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height metodu"
linktitle: "get_Height"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height metodu. C++'da yatay kuralın yüksekliğini alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Yatay kuralın yüksekliğini alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Açıklamalar


Bu, [Height](../../shapebase/get_height/) özelliğine bir kısayoldur.

Geçerli değerler 0 ile 1584 dahil arasında değişir.

Varsayılan değer 1.5.

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

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
