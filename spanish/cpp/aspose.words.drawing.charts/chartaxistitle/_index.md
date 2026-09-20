---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle class. Proporciona acceso a las propiedades del título del eje. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5750
url: /es/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Proporciona acceso a las propiedades del título del eje. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxisTitle : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente del título del eje. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y línea del título del eje. |
| [get_Orientation](./get_orientation/)() | Obtiene o establece la orientación del texto del título del eje. |
| [get_Overlay](./get_overlay/)() | Determina si se permitirá que otros elementos del gráfico se superpongan al título. El valor predeterminado es **false**. |
| [get_Rotation](./get_rotation/)() | Obtiene o establece la rotación del título del eje en grados. |
| [get_Show](./get_show/)() | Determina si se mostrará el título para el eje. El valor predeterminado es **false**. |
| [get_Text](./get_text/)() | Obtiene o establece el texto del título del eje. Si se especifica **null** o un valor vacío, se mostrará un título generado automáticamente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Método set para [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Método set para [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Método set para [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo establecer el título del eje del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Eliminar la serie generada por defecto.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
