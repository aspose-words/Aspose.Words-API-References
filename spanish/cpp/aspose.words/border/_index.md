---
title: "Clase Aspose::Words::Border"
linktitle: "Border"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Border. Representa un borde de un objeto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/border/
---
## Border class


Representa un borde de un objeto. Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Restablece las propiedades del borde a los valores predeterminados. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Determina si el borde especificado es igual en valor al borde actual. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_Color](./get_color/)() | Obtiene o establece el color del borde. |
| [get_DistanceFromText](./get_distancefromtext/)() | Obtiene o establece la distancia del borde al texto o al borde de la página en puntos. |
| [get_IsVisible](./get_isvisible/)() | Devuelve **true** si el [LineStyle](./get_linestyle/) no es [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | Obtiene o establece el estilo del borde. |
| [get_LineWidth](./get_linewidth/)() | Obtiene o establece el ancho del borde en puntos. |
| [get_Shadow](./get_shadow/)() | Obtiene o establece un valor que indica si el borde tiene sombra. |
| [get_ThemeColor](./get_themecolor/)() | Obtiene o establece el color de tema en el esquema de color aplicado que está asociado con este objeto [Border](./). |
| [get_TintAndShade](./get_tintandshade/)() | Obtiene o establece un valor doble que aclara u oscurece un color. |
| [GetHashCode](./gethashcode/)() const override | Sirve como función hash para este tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Establecedor para [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Establecedor para [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Establecedor para [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Establecedor para [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Establecedor para [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Establecedor para [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Establecedor para [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Observaciones


Los bordes pueden aplicarse a varios elementos del documento, incluidos párrafo, secuencia de texto dentro de un párrafo o una celda de tabla.

## Ejemplos



Muestra cómo insertar una cadena rodeada por un borde en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Muestra cómo insertar un párrafo con un borde superior.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Establezca ThemeColor solo cuando LineWidth o LineStyle se hayan establecido.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Ver también

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
