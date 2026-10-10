---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade metodu"
linktitle: "get_NoShade"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade yöntemi. Yatay çizgi için 3B gölgelendirmenin varlığını gösterir. true ise, yatay çizgi 3B gölgelendirme olmadan ve C++'ta katı renk kullanılır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Yatay kural için 3D gölgelendirmenin varlığını gösterir. Eğer **true** ise, yatay kural 3D gölgelendirme olmadan ve katı renk kullanılarak gösterilir.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Açıklamalar


Varsayılan değer **false**'tur.

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
