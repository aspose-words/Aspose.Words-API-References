---
title: "Aspose::Words::Drawing::HorizontalRuleFormat clase"
linktitle: "HorizontalRuleFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat clase. Representa el formato de regla horizontal. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Representa el formato de regla horizontal. Para obtener más información, visite el artículo de documentación [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Obtiene o establece la alineación de la regla horizontal. |
| [get_Color](./get_color/)() | Obtiene o establece el color de pincel que rellena la regla horizontal. |
| [get_Height](./get_height/)() | Obtiene o establece la altura de la regla horizontal. |
| [get_NoShade](./get_noshade/)() | Indica la presencia de sombreado 3D para la regla horizontal. Si **true**, entonces la regla horizontal no tiene sombreado 3D y se utiliza un color sólido. |
| [get_WidthPercent](./get_widthpercent/)() | Obtiene o establece la longitud de la regla horizontal especificada expresada como un porcentaje del ancho de la ventana. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Setter para [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Método setter para [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Método setter para [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Método setter para [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Método setter para [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

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
