---
title: "Aspose::Words::Drawing::Charts::ChartTitle clase"
linktitle: "ChartTitle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle clase. Proporciona acceso a las propiedades del título del gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Proporciona acceso a las propiedades del título del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartTitle : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente del título del gráfico. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y línea del título del gráfico. |
| [get_Orientation](./get_orientation/)() | Obtiene o establece la orientación del texto del título del gráfico. |
| [get_Overlay](./get_overlay/)() | Determina si se permitirá que otros elementos del gráfico se superpongan al título. Por defecto, la superposición es **false**. |
| [get_Rotation](./get_rotation/)() | Obtiene o establece la rotación del título del gráfico en grados. |
| [get_Show](./get_show/)() | Determina si el título debe mostrarse para este gráfico. El valor predeterminado es **true**. |
| [get_Text](./get_text/)() | Obtiene o establece el texto del título del gráfico. Si el valor es **null** o está vacío, se mostrará un título generado automáticamente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter para [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Establecedor de [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Establecedor de [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo insertar un gráfico y establecer un título.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una forma de gráfico con un DocumentBuilder y obtén su gráfico.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Utiliza la propiedad "Title" para dar a nuestro gráfico un título, que aparece en la parte superior central del área del gráfico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Establece la propiedad "Show" a "true" para que el título sea visible.
title->set_Show(true);

// Establece la propiedad "Overlay" a "true". Da más espacio a otros elementos del gráfico permitiendo que se superpongan al título.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
