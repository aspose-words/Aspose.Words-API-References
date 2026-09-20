---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade método"
linktitle: "get_NoShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade. Indica la presencia de sombreado 3D para la regla horizontal. Si es true, entonces la regla horizontal está sin sombreado 3D y se utiliza un color sólido en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Indica la presencia de sombreado 3D para la regla horizontal. Si **true**, entonces la regla horizontal no tiene sombreado 3D y se utiliza un color sólido.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Observaciones


El valor predeterminado es **false**.

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
