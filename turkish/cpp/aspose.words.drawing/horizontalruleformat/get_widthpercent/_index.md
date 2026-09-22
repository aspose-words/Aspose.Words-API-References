---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent yöntemi"
linktitle: "get_WidthPercent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent yöntemi. C++'ta belirtilen yatay çizginin uzunluğunu pencere genişliğinin yüzdesi olarak alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


Belirtilen yatay kuralın uzunluğunu, pencere genişliğinin yüzdesi olarak alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## Açıklamalar


Geçerli değerler 1 ile 100 arasında, her iki uç dahil, aralıktadır.

Varsayılan değer 100'tür.

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
