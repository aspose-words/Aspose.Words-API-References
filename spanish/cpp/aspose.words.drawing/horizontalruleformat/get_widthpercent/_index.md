---
title: "Método Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent"
linktitle: "get_WidthPercent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent. Obtiene o establece la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


Obtiene o establece la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## Observaciones


Los valores válidos van de 1 a 100 inclusive.

El valor predeterminado es 100.

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
