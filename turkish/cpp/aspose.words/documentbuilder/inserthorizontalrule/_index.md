---
title: "Aspose::Words::DocumentBuilder::InsertHorizontalRule metodu"
linktitle: "InsertHorizontalRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertHorizontalRule metodu. C++'da belgeye bir yatay çizgi şekli ekler."
type: docs
weight: 36000
url: /tr/cpp/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder::InsertHorizontalRule method


Belgeye yatay kural şekli ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertHorizontalRule()
```


### ReturnValue

Yatay çizgi olan şekil.

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

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
