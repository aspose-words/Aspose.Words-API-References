---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Format метод"
linktitle: "get_Format"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Format метод. Предоставляет доступ к заполнению и форматированию линий заголовка диаграммы в C++."
type: docs
weight: 1750
url: /ru/cpp/aspose.words.drawing.charts/charttitle/get_format/
---
## ChartTitle::get_Format method


Предоставляет доступ к форматированию заливки и линий заголовка диаграммы.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartTitle::get_Format()
```


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

* Class [ChartFormat](../../chartformat/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
