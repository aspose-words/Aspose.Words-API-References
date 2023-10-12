---
title: Enum ChartSeriesType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartSeriesType opsomming. Gibt einen Typ einer Diagrammreihe an.
type: docs
weight: 800
url: /de/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Gibt einen Typ einer Diagrammreihe an.

```csharp
public enum ChartSeriesType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Area | `0` | Stellt eine Flächendiagrammserie dar. |
| AreaStacked | `1` | Stellt eine gestapelte Flächendiagrammreihe dar. |
| AreaPercentStacked | `2` | Stellt eine 100 % gestapelte Flächendiagrammserie dar. |
| Area3D | `3` | Stellt eine 3D-Flächendiagrammserie dar. |
| Area3DStacked | `4` | Stellt eine gestapelte 3D-Flächendiagrammserie dar. |
| Area3DPercentStacked | `5` | Stellt eine 3D-Diagrammserie mit 100 % gestapelten Flächen dar. |
| Bar | `6` | Stellt eine Balkendiagrammreihe dar. |
| BarStacked | `7` | Stellt eine Reihe gestapelter Balkendiagramme dar. |
| BarPercentStacked | `8` | Stellt eine zu 100 % gestapelte Balkendiagrammreihe dar. |
| Bar3D | `9` | Stellt eine 3D-Balkendiagrammreihe dar. |
| Bar3DStacked | `10` | Stellt eine Reihe gestapelter 3D-Balkendiagramme dar. |
| Bar3DPercentStacked | `11` | Stellt eine 3D-Diagrammreihe mit 100 % gestapelten Balken dar. |
| Bubble | `12` | Stellt eine Blasendiagrammreihe dar. |
| Bubble3D | `13` | Stellt eine 3D-Blasendiagrammserie dar. |
| Column | `14` | Stellt eine Säulendiagrammreihe dar. |
| ColumnStacked | `15` | Stellt eine gestapelte Säulendiagrammreihe dar. |
| ColumnPercentStacked | `16` | Stellt eine zu 100 % gestapelte Säulendiagrammreihe dar. |
| Column3D | `17` | Stellt eine 3D-Säulendiagrammreihe dar. |
| Column3DStacked | `18` | Stellt eine Reihe gestapelter 3D-Säulendiagramme dar. |
| Column3DPercentStacked | `19` | Stellt eine 3D-100 % gestapelte Säulendiagrammserie dar. |
| Column3DClustered | `20` | Stellt eine 3D-Cluster-Säulendiagrammserie dar. |
| Doughnut | `21` | Stellt eine Donut-Diagrammreihe dar. |
| Line | `22` | Stellt eine Liniendiagrammreihe dar. |
| LineStacked | `23` | Stellt eine gestapelte Liniendiagrammserie dar. |
| LinePercentStacked | `24` | Stellt eine 100 % gestapelte Liniendiagrammserie dar. |
| Line3D | `25` | Stellt eine 3D-Liniendiagrammserie dar. |
| Pie | `26` | Stellt eine Kreisdiagrammreihe dar. |
| Pie3D | `27` | Stellt eine 3D-Kreisdiagrammreihe dar. |
| PieOfBar | `28` | Stellt eine Kreis- oder Balkendiagrammreihe dar. |
| PieOfPie | `29` | Stellt eine Kreisdiagrammreihe dar. |
| Radar | `30` | Stellt eine Radarkartenserie dar. |
| Scatter | `31` | Stellt eine Streudiagrammreihe dar. |
| Stock | `32` | Stellt eine Aktiendiagrammserie dar. |
| Surface | `33` | Stellt eine Oberflächendiagrammserie dar. |
| Surface3D | `34` | Stellt eine 3D-Oberflächendiagrammserie dar. |
| Treemap | `35` | Stellt eine Treemap-Diagrammserie dar. |
| Sunburst | `36` | Stellt eine Sunburst-Kartenserie dar. |
| Histogram | `37` | Stellt eine Histogramm-Diagrammreihe dar. |
| Pareto | `38` | Stellt eine Pareto-Diagrammreihe dar. |
| ParetoLine | `39` | Stellt eine Pareto-Liniendiagrammreihe dar. |
| BoxAndWhisker | `40` | Stellt eine Box-and-Whisker-Diagrammserie dar. |
| Waterfall | `41` | Stellt eine Wasserfall-Diagrammserie dar. |
| Funnel | `42` | Stellt eine Trichterdiagrammreihe dar. |
| RegionMap | `43` | Stellt eine Regionskarten-Diagrammserie dar. |

### Beispiele

Zeigt, wie es geht

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Alle Serien vom Typ Column entfernen.
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

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


