---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: .NET için Aspose.Words
description: Dinamik veri görselleştirme için çeşitli seçeneklerle grafik serilerinizi geliştirmek üzere Aspose.Words.Drawing.Charts.ChartSeriesType enum'unu keşfedin.
type: docs
weight: 1110
url: /tr/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Bir grafik serisinin türünü belirtir.

```csharp
public enum ChartSeriesType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Area | `0` | Bir Alan grafik serisini temsil eder. |
| AreaStacked | `1` | Yığılmış Alan grafik serisini temsil eder. |
| AreaPercentStacked | `2` | %100 Yığılmış Alan grafik serisini temsil eder. |
| Area3D | `3` | 3B Alan grafik serisini temsil eder. |
| Area3DStacked | `4` | 3B Yığılmış Alan grafik serisini temsil eder. |
| Area3DPercentStacked | `5` | 3 boyutlu %100 Yığılmış Alan grafik serisini temsil eder. |
| Bar | `6` | Bir Çubuk grafik serisini temsil eder. |
| BarStacked | `7` | Yığılmış Çubuk grafik serisini temsil eder. |
| BarPercentStacked | `8` | %100 Yığılmış Çubuk grafik serisini temsil eder. |
| Bar3D | `9` | 3 boyutlu çubuk grafik serisini temsil eder. |
| Bar3DStacked | `10` | 3B Yığılmış Çubuk grafik serisini temsil eder. |
| Bar3DPercentStacked | `11` | 3 boyutlu %100 Yığılmış Çubuk grafik serisini temsil eder. |
| Bubble | `12` | Bir Balon grafik serisini temsil eder. |
| Bubble3D | `13` | 3 boyutlu bir Kabarcık grafik serisini temsil eder. |
| Column | `14` | Bir Sütun grafik serisini temsil eder. |
| ColumnStacked | `15` | Yığılmış Sütun grafik serisini temsil eder. |
| ColumnPercentStacked | `16` | %100 Yığılmış Sütun grafik serisini temsil eder. |
| Column3D | `17` | 3B Sütun grafik serisini temsil eder. |
| Column3DStacked | `18` | 3B Yığılmış Sütun grafik serisini temsil eder. |
| Column3DPercentStacked | `19` | 3 boyutlu %100 Yığılmış Sütun grafik serisini temsil eder. |
| Column3DClustered | `20` | 3B Kümelenmiş Sütun grafik serisini temsil eder. |
| Doughnut | `21` | Bir Çörek grafik serisini temsil eder. |
| Line | `22` | Bir çizgi grafik serisini temsil eder. |
| LineStacked | `23` | Yığılmış Çizgi grafik serisini temsil eder. |
| LinePercentStacked | `24` | %100 Yığılmış Çizgi grafik serisini temsil eder. |
| Line3D | `25` | 3 boyutlu çizgi grafik serisini temsil eder. |
| Pie | `26` | Bir Pasta grafik serisini temsil eder. |
| Pie3D | `27` | 3 boyutlu pasta grafik serisini temsil eder. |
| PieOfBar | `28` | Çubuk grafik serisinin pastasını temsil eder. |
| PieOfPie | `29` | Pasta grafik serisinin pastasını temsil eder. |
| Radar | `30` | Bir Radar grafik serisini temsil eder. |
| Scatter | `31` | Dağılım grafiği serisini temsil eder. |
| Stock | `32` | Bir Hisse Senedi grafik serisini temsil eder. |
| Surface | `33` | Bir Yüzey grafik serisini temsil eder. |
| Surface3D | `34` | 3B Yüzey grafik serisini temsil eder. |
| Treemap | `35` | Bir Treemap grafik serisini temsil eder. |
| Sunburst | `36` | Bir Sunburst grafik serisini temsil eder. |
| Histogram | `37` | Bir Histogram grafik serisini temsil eder. |
| Pareto | `38` | Bir Pareto grafik serisini temsil eder. |
| ParetoLine | `39` | Bir Pareto Çizgi grafik serisini temsil eder. |
| BoxAndWhisker | `40` | Bir Kutu ve Bıyık grafik serisini temsil eder. |
| Waterfall | `41` | Bir Şelale grafik serisini temsil eder. |
| Funnel | `42` | Bir Huni grafik serisini temsil eder. |
| RegionMap | `43` | Bir Bölge Haritası grafik serisini temsil eder. |

## Örnekler

Belirli grafik serilerinin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Sütun türündeki tüm serileri kaldır.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
