---
title: "Aspose::Words::Drawing::ShapeBase::get_IsHorizontalRule metodu"
linktitle: "get_IsHorizontalRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsHorizontalRule metodu. Bu şekil C++'ta yatay bir kural ise true döndürür."
type: docs
weight: 28000
url: /tr/cpp/aspose.words.drawing/shapebase/get_ishorizontalrule/
---
## ShapeBase::get_IsHorizontalRule method


Bu şekil bir yatay kural ise **true** döndürür.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsHorizontalRule()
```


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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
