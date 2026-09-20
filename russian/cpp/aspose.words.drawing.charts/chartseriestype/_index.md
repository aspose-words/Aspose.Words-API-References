---
title: "Перечисление Aspose::Words::Drawing::Charts::ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::Charts::ChartSeriesType. Указывает тип серии диаграммы в C++."
type: docs
weight: 27500
url: /ru/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Указывает тип серии диаграммы.

```cpp
enum class ChartSeriesType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Area | 0 | Представляет серию диаграммы типа Area. |
| AreaStacked | 1 | Представляет серию диаграммы типа Stacked Area. |
| AreaPercentStacked | 2 | Представляет серию диаграммы типа 100% Stacked Area. |
| Area3D | 3 | Представляет серию диаграммы типа 3D Area. |
| Area3DStacked | 4 | Представляет серию диаграммы типа 3D Stacked Area. |
| Area3DPercentStacked | 5 | Представляет серию диаграммы типа 3D 100% Stacked Area. |
| Bar | 6 | Представляет серию диаграммы типа Bar. |
| BarStacked | 7 | Представляет серию диаграммы типа Stacked Bar. |
| BarPercentStacked | 8 | Представляет серию диаграммы типа 100% Stacked Bar. |
| Bar3D | 9 | Представляет серию диаграммы типа 3D Bar. |
| Bar3DStacked | 10 | Представляет серию диаграммы типа 3D Stacked Bar. |
| Bar3DPercentStacked | 11 | Представляет серию 3D 100% сложенной столбчатой диаграммы. |
| Bubble | 12 | Представляет серию пузырьковой диаграммы. |
| Bubble3D | 13 | Представляет серию 3D пузырьковой диаграммы. |
| Колонка | 14 | Представляет серию столбчатой диаграммы. |
| ColumnStacked | 15 | Представляет серию сложенной столбчатой диаграммы. |
| ColumnPercentStacked | 16 | Представляет серию 100% сложенной столбчатой диаграммы. |
| Column3D | 17 | Представляет серию 3D столбчатой диаграммы. |
| Column3DStacked | 18 | Представляет серию 3D сложенной столбчатой диаграммы. |
| Column3DPercentStacked | 19 | Представляет серию 3D 100% сложенной столбчатой диаграммы. |
| Column3DClustered | 20 | Представляет серию 3D сгруппированной столбчатой диаграммы. |
| Кольцевая диаграмма | 21 | Представляет серию кольцевой диаграммы. |
| Линия | 22 | Представляет серию линейной диаграммы. |
| LineStacked | 23 | Представляет серию сложенной линейной диаграммы. |
| LinePercentStacked | 24 | Представляет серию 100% сложенной линейной диаграммы. |
| Line3D | 25 | Представляет серию 3D линейной диаграммы. |
| Круговая диаграмма | 26 | Представляет серию круговой диаграммы. |
| Pie3D | 27 | Представляет серию 3D круговой диаграммы. |
| PieOfBar | 28 | Представляет серию диаграммы «Круг со столбцами». |
| PieOfPie | 29 | Представляет серию диаграммы «Круг в круге». |
| Радар | 30 | Представляет серию радиальной диаграммы. |
| Точечный | 31 | Представляет серию точечной диаграммы. |
| Акции | 32 | Представляет серию биржевой диаграммы. |
| Поверхность | 33 | Представляет серию поверхностной диаграммы. |
| Surface3D | 34 | Представляет серию 3D поверхностной диаграммы. |
| Дерево-карта | 35 | Представляет серию диаграммы древовидной карты. |
| Солнечный луч | 36 | Представляет серию диаграммы Sunburst. |
| Гистограмма | 37 | Представляет серию диаграммы Histogram. |
| Парето | 38 | Представляет серию диаграммы Pareto. |
| ParetoLine | 39 | Представляет серию диаграммы Pareto Line. |
| BoxAndWhisker | 40 | Представляет серию диаграммы Box and Whisker. |
| Водопад | 41 | Представляет серию диаграммы Waterfall. |
| Воронка | 42 | Представляет серию диаграммы Funnel. |
| RegionMap | 43 | Представляет серию диаграммы Region Map. |


## Примеры



Показывает, как удалить конкретную серию диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Удалить все серии типа Column.
for (int32_t i = chart->get_Series()->get_Count() - 1; i >= 0; i--)
{
    if (chart->get_Series()->idx_get(i)->get_SeriesType() == Aspose::Words::Drawing::Charts::ChartSeriesType::Column)
    {
        chart->get_Series()->RemoveAt(i);
    }
}

chart->get_Series()->Add(u"Aspose Series", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({5.6, 7.1, 2.9, 8.9}));

doc->Save(get_ArtifactsDir() + u"Charts.RemoveSpecificChartSeries.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
