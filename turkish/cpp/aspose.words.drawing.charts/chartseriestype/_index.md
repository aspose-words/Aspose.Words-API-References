---
title: "Aspose::Words::Drawing::Charts::ChartSeriesType enum"
linktitle: "ChartSeriesType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesType enum. C++'da bir grafik serisinin tipini belirtir."
type: docs
weight: 27500
url: /tr/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Bir grafik serisinin tipini belirtir.

```cpp
enum class ChartSeriesType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Area | 0 | Bir Alan grafik serisini temsil eder. |
| AreaStacked | 1 | Bir Yığılmış Alan grafik serisini temsil eder. |
| AreaPercentStacked | 2 | %100 Yığılmış Alan grafik serisini temsil eder. |
| Area3D | 3 | Bir 3D Alan grafik serisini temsil eder. |
| Area3DStacked | 4 | Bir 3D Yığılmış Alan grafik serisini temsil eder. |
| Area3DPercentStacked | 5 | Bir 3D %100 Yığılmış Alan grafik serisini temsil eder. |
| Bar | 6 | Bir Çubuk grafik serisini temsil eder. |
| BarStacked | 7 | Bir Yığılmış Çubuk grafik serisini temsil eder. |
| BarPercentStacked | 8 | %100 Yığılmış Çubuk grafik serisini temsil eder. |
| Bar3D | 9 | Bir 3D Çubuk grafik serisini temsil eder. |
| Bar3DStacked | 10 | Bir 3D Yığılmış Çubuk grafik serisini temsil eder. |
| Bar3DPercentStacked | 11 | 3D %100 Yığılmış Çubuk grafik serisini temsil eder. |
| Bubble | 12 | Balon grafik serisini temsil eder. |
| Bubble3D | 13 | 3D Balon grafik serisini temsil eder. |
| Sütun | 14 | Sütun grafik serisini temsil eder. |
| ColumnStacked | 15 | Yığılmış Sütun grafik serisini temsil eder. |
| ColumnPercentStacked | 16 | %100 Yığılmış Sütun grafik serisini temsil eder. |
| Column3D | 17 | 3D Sütun grafik serisini temsil eder. |
| Column3DStacked | 18 | 3D Yığılmış Sütun grafik serisini temsil eder. |
| Column3DPercentStacked | 19 | 3D %100 Yığılmış Sütun grafik serisini temsil eder. |
| Column3DClustered | 20 | 3D Küme Sütun grafik serisini temsil eder. |
| Doughnut | 21 | Halka grafik serisini temsil eder. |
| Çizgi | 22 | Çizgi grafik serisini temsil eder. |
| LineStacked | 23 | Yığılmış Çizgi grafik serisini temsil eder. |
| LinePercentStacked | 24 | %100 Yığılmış Çizgi grafik serisini temsil eder. |
| Line3D | 25 | 3D Çizgi grafik serisini temsil eder. |
| Pasta | 26 | Pasta grafik serisini temsil eder. |
| Pie3D | 27 | 3D Pasta grafik serisini temsil eder. |
| PieOfBar | 28 | Bar Pasta grafik serisini temsil eder. |
| PieOfPie | 29 | Pasta içinde Pasta grafik serisini temsil eder. |
| Radar | 30 | Radar grafik serisini temsil eder. |
| Saçılım | 31 | Dağılım grafik serisini temsil eder. |
| Stok | 32 | Hisse senedi grafik serisini temsil eder. |
| Yüzey | 33 | Yüzey grafik serisini temsil eder. |
| Yüzey3D | 34 | 3D Yüzey grafik serisini temsil eder. |
| Ağaç Haritası | 35 | Ağaç haritası grafik serisini temsil eder. |
| Güneş Patlaması | 36 | Bir Sunburst grafik serisini temsil eder. |
| Histogram | 37 | Bir Histogram grafik serisini temsil eder. |
| Pareto | 38 | Bir Pareto grafik serisini temsil eder. |
| ParetoLine | 39 | Bir Pareto Line grafik serisini temsil eder. |
| KutuVeBıyık | 40 | Bir Box and Whisker grafik serisini temsil eder. |
| Şelale | 41 | Bir Waterfall grafik serisini temsil eder. |
| Huni | 42 | Bir Funnel grafik serisini temsil eder. |
| RegionMap | 43 | Bir Region Map grafik serisini temsil eder. |


## Örnekler



Belirli bir grafik serisini kaldırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Sütun tipindeki tüm serileri kaldır.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
