---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataTable класс. Позволяет задавать свойства таблицы данных диаграммы в C++."
type: docs
weight: 9500
url: /ru/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Позволяет указать свойства таблицы данных диаграммы.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Font](./get_font/)() | Обеспечивает доступ к форматированию шрифта таблицы данных. |
| [get_Format](./get_format/)() | Обеспечивает доступ к заливке фона текста и форматированию границы таблицы данных. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Получает или задает флаг, указывающий, отображается ли горизонтальная граница таблицы данных. Значение по умолчанию — **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Получает или задает флаг, указывающий, отображаются ли ключи легенды в таблице данных. Значение по умолчанию — **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Получает или задает флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий рядов и категорий. Значение по умолчанию — **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Получает или задает флаг, указывающий, отображается ли вертикальная граница таблицы данных. Значение по умолчанию — **true**. |
| [get_Show](./get_show/)() const | Получает или задает флаг, указывающий, будет ли таблица данных отображаться для диаграммы. Значение по умолчанию — **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как отобразить таблицу данных с данными рядов диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
