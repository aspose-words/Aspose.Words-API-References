---
title: "Aspose::Words::Drawing::Charts::AxisScaling класс"
linktitle: "AxisScaling"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::AxisScaling класс. Представляет параметры масштабирования оси. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class


Представляет параметры масштабирования оси. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisScaling : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [AxisScaling](./axisscaling/)() |  |
| [get_LogBase](./get_logbase/)() const | Получает или задает логарифмическую основу для логарифмической оси. |
| [get_Maximum](./get_maximum/)() | Получает или задает максимальное значение оси. |
| [get_Minimum](./get_minimum/)() | Получает или задает минимальное значение оси. |
| [get_Type](./get_type/)() const | Получает или задает тип масштабирования оси. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_LogBase](./set_logbase/)(double) | Сеттер для [Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase](./get_logbase/). |
| [set_Maximum](./set_maximum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Сеттер для [Aspose::Words::Drawing::Charts::AxisScaling::get_Maximum](./get_maximum/). |
| [set_Minimum](./set_minimum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Сеттер для [Aspose::Words::Drawing::Charts::AxisScaling::get_Minimum](./get_minimum/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::Charts::AxisScaleType) | Сеттер для [Aspose::Words::Drawing::Charts::AxisScaling::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как применить логарифмическое масштабирование к оси диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Вставьте серию с координатами X/Y для пяти точек.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// Масштабирование оси X по умолчанию линейное,
// отображая равномерно увеличивающиеся значения, охватывающие наш диапазон X (0, 1, 2, 3...).
// Линейная ось не идеальна для наших значений Y
// поскольку точки с меньшими значениями Y будет труднее читать.
// Логарифмическое масштабирование с основанием 20 (1, 20, 400, 8000...)
// распространит построенные точки, позволяя легче считывать их значения на диаграмме.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
