---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition перечисление"
linktitle: "ChartDataLabelPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition перечисление. Указывает положение подписи данных диаграммы в C++."
type: docs
weight: 27334
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Указывает позицию подписи данных на диаграмме.

```cpp
enum class ChartDataLabelPosition
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| По центру | 0 | Указывает, что подпись данных должна отображаться по центру маркера данных. |
| Слева | 1 | Указывает, что подпись данных должна отображаться слева от маркера данных. |
| Справа | 2 | Указывает, что подпись данных должна отображаться справа от маркера данных. |
| Выше | 3 | Указывает, что подпись данных должна отображаться над маркером данных. |
| Ниже | 4 | Указывает, что подпись данных должна отображаться под маркером данных. |
| InsideBase | 5 | Указывает, что подпись данных должна отображаться внутри основания маркера данных. |
| InsideEnd | 6 | Указывает, что подпись данных должна отображаться внутри конца маркера данных. |
| OutsideEnd | 7 | Указывает, что подпись данных должна отображаться за пределами конца маркера данных. |
| Оптимальное соответствие | 8 | Указывает, что подпись данных должна отображаться в наиболее подходящей позиции. |


## Примеры



Показывает, как задать позицию подписи данных.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставить столбчатую диаграмму.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Удалить автоматически сгенерированную серию.
seriesColl->Clear();

// Добавить серию.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Показать подписи данных и задать цвет шрифта.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Задать позицию подписи данных.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
