---
title: "Метод Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource"
linktitle: "get_IsLinkedToSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource. Указывает, связан ли код формата с исходной ячейкой. По умолчанию true в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing.charts/chartnumberformat/get_islinkedtosource/
---
## ChartNumberFormat::get_IsLinkedToSource method


Указывает, связан ли код формата с исходной ячейкой. По умолчанию true.

```cpp
bool Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource()
```


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

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
