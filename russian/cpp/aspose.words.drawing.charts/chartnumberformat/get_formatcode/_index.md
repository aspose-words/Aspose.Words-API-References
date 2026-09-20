---
title: "Метод Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode"
linktitle: "get_FormatCode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode. Получает или задает код формата, применяемый к метке данных в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Получает или задает код формата, применяемый к подписи данных.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Примечания


Форматирование чисел используется для изменения отображения значения в метке данных и может применяться самыми креативными способами. Примеры числовых форматов:

Число - "#,##0.00"

Валюта - "\"\$\\"#,##0.00"

Время - "[$-x-systime]h:mm:ss AM/PM"

Дата - "d/mm/yyyy"

Процент - "0.00%"

Дробь - "# ?/?"

Экспоненциальный - "0.00E+00"

Текст - "@"

Бухгалтерский - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Пользовательский с цветом - "[Red]-#,##0.0"

## Примеры



Показывает, как включить и настроить подписи данных для серии диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте линейную диаграмму, затем очистите её демонстрационные данные серии, чтобы начать с чистой диаграммы,
// а затем задайте заголовок.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Вставьте пользовательскую серию диаграммы с месяцами в качестве категорий для оси X,
// и соответствующими десятичными значениями для оси Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Включите подписи данных, а затем примените пользовательский числовой формат для значений, отображаемых в подписях данных.
// Этот формат будет воспринимать отображаемые десятичные значения как миллионы долларов США.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```


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
