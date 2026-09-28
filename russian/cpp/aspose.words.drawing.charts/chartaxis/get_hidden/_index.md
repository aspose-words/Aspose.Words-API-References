---
title: "Метод Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden"
linktitle: "get_Hidden"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden. Получает или задает флаг, указывающий, скрыта ли эта ось в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


Получает или задает флаг, указывающий, скрыта ли эта ось.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## Примеры



Показывает, как скрыть оси диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Добавьте пользовательскую серию с категориями для оси X и соответствующими десятичными значениями для оси Y.
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// Скройте оси диаграммы, чтобы упростить её внешний вид.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## См. также

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
