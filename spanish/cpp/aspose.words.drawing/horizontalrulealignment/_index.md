---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment enum"
linktitle: "HorizontalRuleAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment enum. Representa la alineación para la regla horizontal especificada en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Representa la alineación para la regla horizontal especificada.

```cpp
enum class HorizontalRuleAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Izquierda | 0 | Alineado a la izquierda. |
| Centro | 1 | Alineado al centro. |
| Derecha | 2 | Alineado a la derecha. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
