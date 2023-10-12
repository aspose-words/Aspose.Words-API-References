---
title: Enum ChartSeriesType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartSeriesType uppräkning. Anger en typ av en diagramserie.
type: docs
weight: 800
url: /sv/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Anger en typ av en diagramserie.

```csharp
public enum ChartSeriesType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Area | `0` | Representerar en områdesdiagramserie. |
| AreaStacked | `1` | Representerar en stapeldiagramserie. |
| AreaPercentStacked | `2` | Representerar en diagramserie med 100 % staplade ytor. |
| Area3D | `3` | Representerar en 3D-områdesdiagramserie. |
| Area3DStacked | `4` | Representerar en 3D-diagramserie med staplade ytor. |
| Area3DPercentStacked | `5` | Representerar en 3D-serie med 100 % staplade ytor. |
| Bar | `6` | Representerar en stapeldiagramserie. |
| BarStacked | `7` | Representerar en staplad stapeldiagramserie. |
| BarPercentStacked | `8` | Representerar en 100 % staplad stapeldiagramserie. |
| Bar3D | `9` | Representerar en 3D stapeldiagramserie. |
| Bar3DStacked | `10` | Representerar en 3D-staplad stapeldiagramserie. |
| Bar3DPercentStacked | `11` | Representerar en 3D 100 % staplad stapeldiagramserie. |
| Bubble | `12` | Representerar en bubbeldiagramserie. |
| Bubble3D | `13` | Representerar en 3D-bubblediagramserie. |
| Column | `14` | Representerar en kolumndiagramserie. |
| ColumnStacked | `15` | Representerar en diagramserie med staplade kolumner. |
| ColumnPercentStacked | `16` | Representerar en 100 % staplad kolumndiagramserie. |
| Column3D | `17` | Representerar en 3D-kolonndiagramserie. |
| Column3DStacked | `18` | Representerar en diagramserie med staplade kolumner i 3D. |
| Column3DPercentStacked | `19` | Representerar en 3D-serie med 100 % staplade kolumner. |
| Column3DClustered | `20` | Representerar en 3D-klustrad kolumndiagramserie. |
| Doughnut | `21` | Representerar en munkdiagramserie. |
| Line | `22` | Representerar en linjediagramserie. |
| LineStacked | `23` | Representerar en stapeldiagramserie. |
| LinePercentStacked | `24` | Representerar en 100 % staplad linjediagramserie. |
| Line3D | `25` | Representerar en 3D-linjediagramserie. |
| Pie | `26` | Representerar en cirkeldiagramserie. |
| Pie3D | `27` | Representerar en 3D-cirkeldiagramserie. |
| PieOfBar | `28` | Representerar en serie av stapeldiagram. |
| PieOfPie | `29` | Representerar en cirkeldiagramserie. |
| Radar | `30` | Representerar en radardiagramserie. |
| Scatter | `31` | Representerar en scatter-diagramserie. |
| Stock | `32` | Representerar en aktiediagramserie. |
| Surface | `33` | Representerar en ytdiagramserie. |
| Surface3D | `34` | Representerar en 3D Surface-diagramserie. |
| Treemap | `35` | Representerar en trädkarta-diagramserie. |
| Sunburst | `36` | Representerar en Sunburst-diagramserie. |
| Histogram | `37` | Representerar en histogramdiagramserie. |
| Pareto | `38` | Representerar en Pareto-diagramserie. |
| ParetoLine | `39` | Representerar en Pareto Line-diagramserie. |
| BoxAndWhisker | `40` | Representerar en box- och morrhårsdiagramserie. |
| Waterfall | `41` | Representerar en vattenfallsdiagramserie. |
| Funnel | `42` | Representerar en trattdiagramserie. |
| RegionMap | `43` | Representerar en områdeskartserie. |

### Exempel

Visar hur man

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Ta bort alla serier av kolumntypen.
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

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


