---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShadowFormat class. Representa el formato de sombra para un objeto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Representa el formato de sombra para un objeto. Para obtener más información, visite el artículo de documentación [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class ShadowFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Borra el formato de sombra. |
| [get_Color](./get_color/)() | Obtiene o establece un objeto **Color** que representa el color de la sombra. El valor predeterminado es **Black**. |
| [get_Transparency](./get_transparency/)() | Obtiene o establece el grado de transparencia del efecto de sombra como un valor entre 0.0 (opaco) y 1.0 (claro). El valor predeterminado es 0.0. |
| [get_Type](./get_type/)() | Obtiene o establece el [ShadowType](../shadowtype/) especificado para [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Devuelve **true** si el formato aplicado a esta instancia es visible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Establecedor para [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Establecedor para [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Establecedor para [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo obtener el color de la sombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
