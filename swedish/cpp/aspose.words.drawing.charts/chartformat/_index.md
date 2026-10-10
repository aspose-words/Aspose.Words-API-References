---
title: "Aspose::Words::Drawing::Charts::ChartFormat klass"
linktitle: "ChartFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartFormat klass. Representerar formateringen av ett diagramelement. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Representerar formateringen av ett diagramelement. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Fill](./get_fill/)() | Hämtar fyllningsformatering för det överordnade diagramelementet. |
| [get_IsDefined](./get_isdefined/)() | Hämtar en flagga som indikerar om någon formatering är definierad. |
| [get_ShapeType](./get_shapetype/)() | Hämtar eller anger formtypen för det överordnade diagramelementet. |
| [get_Stroke](./get_stroke/)() | Hämtar linjeformatering för det överordnade diagramelementet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | Sättare för [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | Återställer fyllningen av diagramelementet till standardvärdet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man använder diagramformatering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Ta bort serier som genereras som standard.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Formatera diagrambakgrund.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Dölj axelns tick-etiketter.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Formatera diagramtitel.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatera axeltitel.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatera förklaring.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
