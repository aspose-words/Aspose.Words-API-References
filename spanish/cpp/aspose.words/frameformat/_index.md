---
title: "Clase Aspose::Words::FrameFormat"
linktitle: "FrameFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::FrameFormat. Representa el formato relacionado con el marco para un párrafo en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words/frameformat/
---
## FrameFormat class


Representa el formato relacionado con el marco para un párrafo.

```cpp
class FrameFormat : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Height](./get_height/)() | Obtiene la altura del marco especificado. |
| [get_HeightRule](./get_heightrule/)() | Obtiene la regla para determinar la altura del marco especificado. |
| [get_HorizontalAlignment](./get_horizontalalignment/)() | Obtiene la alineación horizontal del marco especificado. |
| [get_HorizontalDistanceFromText](./get_horizontaldistancefromtext/)() | Obtiene la distancia horizontal entre un marco y el texto circundante, en puntos. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Obtiene la distancia horizontal entre el borde del marco y el elemento especificado por la propiedad [RelativeHorizontalPosition](./get_relativehorizontalposition/). |
| [get_IsFrame](./get_isframe/)() | Devuelve **true** si el párrafo es un marco. |
| [get_RelativeHorizontalPosition](./get_relativehorizontalposition/)() | Obtiene la posición horizontal relativa de un marco. |
| [get_RelativeVerticalPosition](./get_relativeverticalposition/)() | Obtiene la posición vertical relativa de un marco. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Obtiene la alineación vertical del marco especificado. |
| [get_VerticalDistanceFromText](./get_verticaldistancefromtext/)() | Especifica la distancia vertical (en puntos) entre un marco y el texto circundante. |
| [get_VerticalPosition](./get_verticalposition/)() | Obtiene la distancia vertical entre el borde del marco y el elemento especificado por la propiedad [RelativeVerticalPosition](./get_relativeverticalposition/). |
| [get_Width](./get_width/)() | Obtiene el ancho del marco especificado, en puntos. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


Este objeto siempre se crea. Si un párrafo es un marco, entonces todas las propiedades contendrán sus respectivos valores; de lo contrario, todas las propiedades se establecen en sus valores predeterminados.

Utilice [IsFrame](./get_isframe/) para comprobar si el párrafo es un marco.

## Ejemplos



Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son marcos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraph frame.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraphFrame = doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_FrameFormat()->get_IsFrame();
})));

ASPOSE_ASSERT_EQ(233.3, paragraphFrame->get_FrameFormat()->get_Width());
ASPOSE_ASSERT_EQ(138.8, paragraphFrame->get_FrameFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::AtLeast, paragraphFrame->get_FrameFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::Drawing::HorizontalAlignment::Default, paragraphFrame->get_FrameFormat()->get_HorizontalAlignment());
ASSERT_EQ(Aspose::Words::Drawing::VerticalAlignment::Default, paragraphFrame->get_FrameFormat()->get_VerticalAlignment());
ASPOSE_ASSERT_EQ(34.05, paragraphFrame->get_FrameFormat()->get_HorizontalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Page, paragraphFrame->get_FrameFormat()->get_RelativeHorizontalPosition());
ASPOSE_ASSERT_EQ(9.0, paragraphFrame->get_FrameFormat()->get_HorizontalDistanceFromText());
ASPOSE_ASSERT_EQ(20.5, paragraphFrame->get_FrameFormat()->get_VerticalPosition());
ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, paragraphFrame->get_FrameFormat()->get_RelativeVerticalPosition());
ASPOSE_ASSERT_EQ(0.0, paragraphFrame->get_FrameFormat()->get_VerticalDistanceFromText());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
