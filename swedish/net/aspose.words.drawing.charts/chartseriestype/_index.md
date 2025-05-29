---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Drawing.Charts.ChartSeriesType för att förbättra dina diagramserier med olika alternativ för dynamisk datavisualisering.
type: docs
weight: 1110
url: /sv/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Anger en typ av diagramserie.

```csharp
public enum ChartSeriesType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Area | `0` | Representerar en ytdiagramserie. |
| AreaStacked | `1` | Representerar en diagramserie med staplade ytor. |
| AreaPercentStacked | `2` | Representerar en diagramserie med 100 % staplad yta. |
| Area3D | `3` | Representerar en 3D-areadiagramserie. |
| Area3DStacked | `4` | Representerar en 3D-stapelad areadiagramserie. |
| Area3DPercentStacked | `5` | Representerar en 3D-diagramserie med 100 % staplad yta. |
| Bar | `6` | Representerar en stapeldiagramserie. |
| BarStacked | `7` | Representerar en staplad stapeldiagramserie. |
| BarPercentStacked | `8` | Representerar en 100 % staplad stapeldiagramserie. |
| Bar3D | `9` | Representerar en 3D-stapeldiagramserie. |
| Bar3DStacked | `10` | Representerar en 3D-staplad stapeldiagramserie. |
| Bar3DPercentStacked | `11` | Representerar en 3D 100 % staplad stapeldiagramserie. |
| Bubble | `12` | Representerar en bubbeldiagramserie. |
| Bubble3D | `13` | Representerar en 3D-bubbeldiagramserie. |
| Column | `14` | Representerar en stapeldiagramserie. |
| ColumnStacked | `15` | Representerar en staplad kolumndiagramserie. |
| ColumnPercentStacked | `16` | Representerar en 100 % staplad stapeldiagramserie. |
| Column3D | `17` | Representerar en 3D-stapeldiagramserie. |
| Column3DStacked | `18` | Representerar en 3D-staplad kolumndiagramserie. |
| Column3DPercentStacked | `19` | Representerar en 3D 100 % staplad stapeldiagramserie. |
| Column3DClustered | `20` | Representerar en 3D-klustrad stapeldiagramserie. |
| Doughnut | `21` | Representerar en ringdiagramserie. |
| Line | `22` | Representerar en linjediagramserie. |
| LineStacked | `23` | Representerar en staplad linjediagramserie. |
| LinePercentStacked | `24` | Representerar en 100 % staplad linjediagramserie. |
| Line3D | `25` | Representerar en 3D-linjediagramserie. |
| Pie | `26` | Representerar en cirkeldiagramserie. |
| Pie3D | `27` | Representerar en serie 3D-cirkeldiagram. |
| PieOfBar | `28` | Representerar en cirkeldiagram- eller stapeldiagramserie. |
| PieOfPie | `29` | Representerar en cirkeldiagramserie. |
| Radar | `30` | Representerar en radardiagramserie. |
| Scatter | `31` | Representerar en punktdiagramserie. |
| Stock | `32` | Representerar en aktiediagramserie. |
| Surface | `33` | Representerar en serie Surface-diagram. |
| Surface3D | `34` | Representerar en 3D-ytediagramserie. |
| Treemap | `35` | Representerar en trädkartserie. |
| Sunburst | `36` | Representerar en Sunburst-diagramserie. |
| Histogram | `37` | Representerar en histogramdiagramserie. |
| Pareto | `38` | Representerar en Pareto-diagramserie. |
| ParetoLine | `39` | Representerar en Pareto Line-diagramserie. |
| BoxAndWhisker | `40` | Representerar en Box and Whisker-diagramserie. |
| Waterfall | `41` | Representerar en vattenfallsdiagramserie. |
| Funnel | `42` | Representerar en trattdiagramserie. |
| RegionMap | `43` | Representerar en regionskartserie. |

## Exempel

Visar hur man tar bort specifika diagramserier.

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
