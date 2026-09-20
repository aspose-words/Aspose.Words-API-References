---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height método"
linktitle: "get_Height"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height método. Obtiene o establece la altura de la regla horizontal en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Obtiene o establece la altura de la regla horizontal.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Observaciones


Este es un acceso directo a la propiedad [Height](../../shapebase/get_height/).

Los valores válidos van de 0 a 1584 inclusive.

El valor predeterminado es 1.5.

## Ejemplos



Muestra cómo insertar una forma de regla horizontal y personalizar su formato.
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

## Ver también

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
