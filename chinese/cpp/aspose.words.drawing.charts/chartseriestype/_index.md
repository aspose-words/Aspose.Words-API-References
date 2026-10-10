---
title: "Aspose::Words::Drawing::Charts::ChartSeriesType enum"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesType 枚举。指定 C++ 中图表系列的类型。"
type: docs
weight: 27500
url: /zh/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


指定图表系列的类型。

```cpp
enum class ChartSeriesType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Area | 0 | 表示一个面积图系列。 |
| AreaStacked | 1 | 表示一个堆积面积图系列。 |
| AreaPercentStacked | 2 | 表示一个 100% 堆积面积图系列。 |
| Area3D | 3 | 表示一个 3D 面积图系列。 |
| Area3DStacked | 4 | 表示一个 3D 堆积面积图系列。 |
| Area3DPercentStacked | 5 | 表示一个 3D 100% 堆积面积图系列。 |
| Bar | 6 | 表示一个条形图系列。 |
| BarStacked | 7 | 表示一个堆积条形图系列。 |
| BarPercentStacked | 8 | 表示一个 100% 堆积条形图系列。 |
| Bar3D | 9 | 表示一个 3D 条形图系列。 |
| Bar3DStacked | 10 | 表示一个 3D 堆积条形图系列。 |
| Bar3DPercentStacked | 11 | 表示一个 3D 100% 堆积条形图系列。 |
| 气泡 | 12 | 表示一个气泡图系列。 |
| Bubble3D | 13 | 表示一个 3D 气泡图系列。 |
| 列 | 14 | 表示一个柱形图系列。 |
| ColumnStacked | 15 | 表示一个堆积柱形图系列。 |
| ColumnPercentStacked | 16 | 表示一个 100% 堆积柱形图系列。 |
| Column3D | 17 | 表示一个 3D 柱形图系列。 |
| Column3DStacked | 18 | 表示一个 3D 堆积柱形图系列。 |
| Column3DPercentStacked | 19 | 表示一个 3D 100% 堆积柱形图系列。 |
| Column3DClustered | 20 | 表示一个 3D 簇状柱形图系列。 |
| 环形图 | 21 | 表示一个环形图系列。 |
| 线 | 22 | 表示一个折线图系列。 |
| LineStacked | 23 | 表示一个堆叠折线图系列。 |
| LinePercentStacked | 24 | 表示一个 100% 堆叠折线图系列。 |
| Line3D | 25 | 表示一个 3D 折线图系列。 |
| 饼图 | 26 | 表示一个饼图系列。 |
| Pie3D | 27 | 表示一个 3D 饼图系列。 |
| PieOfBar | 28 | 表示一个柱形图的饼图系列。 |
| PieOfPie | 29 | 表示一个饼图的饼图系列。 |
| Radar | 30 | 表示一个雷达图系列。 |
| Scatter | 31 | 表示一个散点图系列。 |
| Stock | 32 | 表示一个股票图系列。 |
| Surface | 33 | 表示一个曲面图系列。 |
| Surface3D | 34 | 表示一个 3D 曲面图系列。 |
| Treemap | 35 | 表示一个树状图系列。 |
| Sunburst | 36 | 表示一个旭日图系列。 |
| 直方图 | 37 | 表示一个直方图系列。 |
| 帕累托 | 38 | 表示一个帕累托图系列。 |
| ParetoLine | 39 | 表示一个帕累托线图系列。 |
| 箱线图 | 40 | 表示一个箱线图系列。 |
| 瀑布图 | 41 | 表示一个瀑布图系列。 |
| 漏斗 | 42 | 表示一个漏斗图系列。 |
| RegionMap | 43 | 表示一个区域地图系列。 |


## 示例



展示如何删除特定的图表系列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// 删除所有柱形类型的系列。
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

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
