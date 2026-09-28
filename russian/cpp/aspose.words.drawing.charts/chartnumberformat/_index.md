---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat класс"
linktitle: "ChartNumberFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat class. Представляет форматирование чисел родительского элемента. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


Представляет числовое форматирование родительского элемента. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartNumberFormat : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | Получает или задает код формата, применяемый к подписи данных. |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | Указывает, связан ли код формата с исходной ячейкой. По умолчанию true. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/). |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как установить форматирование значений диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Добавьте пользовательскую серию к диаграмме с категориями для оси X,
// и большими соответствующими числовыми значениями для оси Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Установите числовой формат меток делений оси Y так, чтобы цифры не группировались запятыми.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Этот флаг может переопределить вышеуказанное значение и взять числовой формат из исходной ячейки.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
