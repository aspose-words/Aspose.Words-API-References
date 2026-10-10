---
title: "Aspose::Words::BorderCollection clase"
linktitle: "BorderCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BorderCollection clase. Una colección de objetos Border. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/bordercollection/
---
## BorderCollection class


Una colección de objetos [Border](../border/). Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Elimina todos los bordes de un objeto. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Compara colecciones de bordes. |
| [get_Bottom](./get_bottom/)() | Obtiene el borde inferior. |
| [get_Color](./get_color/)() | Obtiene o establece el color del borde. |
| [get_Count](./get_count/)() | Obtiene el número de bordes en la colección. |
| [get_DistanceFromText](./get_distancefromtext/)() | Obtiene o establece la distancia del borde al texto en puntos. |
| [get_Horizontal](./get_horizontal/)() | Obtiene el borde horizontal que se usa entre celdas o párrafos conformes. |
| [get_Left](./get_left/)() | Obtiene el borde izquierdo. |
| [get_LineStyle](./get_linestyle/)() | Obtiene o establece el estilo del borde. |
| [get_LineWidth](./get_linewidth/)() | Obtiene o establece el ancho del borde en puntos. |
| [get_Right](./get_right/)() | Obtiene el borde derecho. |
| [get_Shadow](./get_shadow/)() | Obtiene o establece un valor que indica si el borde tiene sombra. |
| [get_Top](./get_top/)() | Obtiene el borde superior. |
| [get_Vertical](./get_vertical/)() | Obtiene el borde vertical que se usa entre celdas. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los bordes de la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Recupera un objeto [Border](../border/) por tipo de borde. |
| [idx_get](./idx_get/)(int32_t) | Recupera un objeto [Border](../border/) por índice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Método set de [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Método set de [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Método set de [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Método set de [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Método set para [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Ejemplos



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
