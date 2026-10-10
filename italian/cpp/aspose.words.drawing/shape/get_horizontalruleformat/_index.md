---
title: "Metodo Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat"
linktitle: "get_HorizontalRuleFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat. Fornisce l'accesso alle proprietà della forma di regola orizzontale. Per una forma che non è una regola orizzontale, restituisce null in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing/shape/get_horizontalruleformat/
---
## Shape::get_HorizontalRuleFormat method


Fornisce l'accesso alle proprietà della forma di regola orizzontale. Per una forma che non è una regola orizzontale, restituisce **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat()
```


## Esempi



Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.
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

## Vedi anche

* Class [HorizontalRuleFormat](../../horizontalruleformat/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
