---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.Charts.ChartSeriesType, um Ihre Diagrammserie mit verschiedenen Optionen zur dynamischen Datenvisualisierung zu erweitern.
type: docs
weight: 1110
url: /de/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Gibt den Typ einer Diagrammreihe an.

```csharp
public enum ChartSeriesType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Area | `0` | Stellt eine Flächendiagrammreihe dar. |
| AreaStacked | `1` | Stellt eine gestapelte Flächendiagrammreihe dar. |
| AreaPercentStacked | `2` | Stellt eine 100 % gestapelte Flächendiagrammreihe dar. |
| Area3D | `3` | Stellt eine 3D-Flächendiagrammreihe dar. |
| Area3DStacked | `4` | Stellt eine 3D-gestapelte Flächendiagrammreihe dar. |
| Area3DPercentStacked | `5` | Stellt eine 3D-Diagrammreihe mit 100 % gestapelter Fläche dar. |
| Bar | `6` | Stellt eine Balkendiagrammreihe dar. |
| BarStacked | `7` | Stellt eine gestapelte Balkendiagrammreihe dar. |
| BarPercentStacked | `8` | Stellt eine 100 % gestapelte Balkendiagrammreihe dar. |
| Bar3D | `9` | Stellt eine 3D-Balkendiagrammreihe dar. |
| Bar3DStacked | `10` | Stellt eine 3D-gestapelte Balkendiagrammreihe dar. |
| Bar3DPercentStacked | `11` | Stellt eine 3D-100 % gestapelte Balkendiagrammreihe dar. |
| Bubble | `12` | Stellt eine Blasendiagrammreihe dar. |
| Bubble3D | `13` | Stellt eine 3D-Blasendiagrammreihe dar. |
| Column | `14` | Stellt eine Säulendiagrammreihe dar. |
| ColumnStacked | `15` | Stellt eine gestapelte Säulendiagrammreihe dar. |
| ColumnPercentStacked | `16` | Stellt eine 100 % gestapelte Säulendiagrammreihe dar. |
| Column3D | `17` | Stellt eine 3D-Säulendiagrammreihe dar. |
| Column3DStacked | `18` | Stellt eine 3D-gestapelte Säulendiagrammreihe dar. |
| Column3DPercentStacked | `19` | Stellt eine 3D-100 % gestapelte Säulendiagrammreihe dar. |
| Column3DClustered | `20` | Stellt eine 3D-Säulendiagrammreihe dar. |
| Doughnut | `21` | Stellt eine Ringdiagrammreihe dar. |
| Line | `22` | Stellt eine Liniendiagrammreihe dar. |
| LineStacked | `23` | Stellt eine gestapelte Liniendiagrammreihe dar. |
| LinePercentStacked | `24` | Stellt eine 100 % gestapelte Liniendiagrammreihe dar. |
| Line3D | `25` | Stellt eine 3D-Liniendiagrammreihe dar. |
| Pie | `26` | Stellt eine Kreisdiagrammreihe dar. |
| Pie3D | `27` | Stellt eine 3D-Kreisdiagrammreihe dar. |
| PieOfBar | `28` | Stellt eine Kreis- oder Balkendiagrammreihe dar. |
| PieOfPie | `29` | Stellt eine Kreisdiagrammreihe dar. |
| Radar | `30` | Stellt eine Radardiagrammserie dar. |
| Scatter | `31` | Stellt eine Streudiagrammreihe dar. |
| Stock | `32` | Stellt eine Aktienchartreihe dar. |
| Surface | `33` | Stellt eine Oberflächendiagrammreihe dar. |
| Surface3D | `34` | Stellt eine 3D-Oberflächendiagrammreihe dar. |
| Treemap | `35` | Stellt eine Treemap-Diagrammreihe dar. |
| Sunburst | `36` | Stellt eine Sunburst-Diagrammreihe dar. |
| Histogram | `37` | Stellt eine Histogramm-Diagrammreihe dar. |
| Pareto | `38` | Stellt eine Pareto-Diagrammreihe dar. |
| ParetoLine | `39` | Stellt eine Pareto-Liniendiagrammreihe dar. |
| BoxAndWhisker | `40` | Stellt eine Box-and-Whisker-Diagrammreihe dar. |
| Waterfall | `41` | Stellt eine Wasserfalldiagrammreihe dar. |
| Funnel | `42` | Stellt eine Trichterdiagrammreihe dar. |
| RegionMap | `43` | Stellt eine Diagrammreihe einer Regionskarte dar. |

## Beispiele

Zeigt, wie bestimmte Diagrammreihen entfernt werden.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Alle Reihen des Spaltentyps entfernen.
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
