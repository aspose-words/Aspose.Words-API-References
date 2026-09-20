---
title: "Aspose::Words::Drawing::Charts::ChartFormat класс"
linktitle: "ChartFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat класс. Представляет форматирование элемента диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Представляет форматирование элемента диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Fill](./get_fill/)() | Получает формат заливки для родительского элемента диаграммы. |
| [get_IsDefined](./get_isdefined/)() | Получает флаг, указывающий, определён ли какой-либо формат. |
| [get_ShapeType](./get_shapetype/)() | Получает или задаёт тип формы родительского элемента диаграммы. |
| [get_Stroke](./get_stroke/)() | Получает формат линии для родительского элемента диаграммы. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | Сеттер для [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | Сбрасывает заливку элемента диаграммы к значению по умолчанию. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как использовать форматирование диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Удалить серию, созданную по умолчанию.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Отформатировать фон диаграммы.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Скрыть подписи делений оси.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Отформатировать заголовок диаграммы.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Отформатировать заголовок оси.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Отформатировать легенду.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
