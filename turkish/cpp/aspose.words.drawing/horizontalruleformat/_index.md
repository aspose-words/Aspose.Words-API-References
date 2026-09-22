---
title: "Aspose::Words::Drawing::HorizontalRuleFormat class"
linktitle: "HorizontalRuleFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalRuleFormat sınıfı. Yatay kural biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için C++'daki belgelendirme makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Yatay kural biçimlendirmesini temsil eder. Daha fazla bilgi için, [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) dokümantasyon makalesini ziyaret edin.

```cpp
class HorizontalRuleFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Yatay kuralın hizalamasını alır veya ayarlar. |
| [get_Color](./get_color/)() | Yatay kuralı dolduran fırça rengini alır veya ayarlar. |
| [get_Height](./get_height/)() | Yatay kuralın yüksekliğini alır veya ayarlar. |
| [get_NoShade](./get_noshade/)() | Yatay kural için 3D gölgelendirmenin varlığını gösterir. Eğer **true** ise, yatay kural 3D gölgelendirme olmadan ve katı renk kullanılarak gösterilir. |
| [get_WidthPercent](./get_widthpercent/)() | Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Ayarlayıcı, [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/) için. |
| [set_Color](./set_color/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Ayarlayıcı [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Ayarlayıcı [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

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
