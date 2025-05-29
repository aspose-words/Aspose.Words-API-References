---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.Drawing.Charts.ChartType, um verschiedene Diagrammtypen zu entdecken und die Datenvisualisierung Ihres Dokuments mühelos zu verbessern.
type: docs
weight: 1150
url: /de/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Gibt den Typ eines Diagramms an.

```csharp
public enum ChartType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Area | `0` | Flächendiagramm. |
| AreaStacked | `1` | Gestapeltes Flächendiagramm. |
| AreaPercentStacked | `2` | 100 % gestapeltes Flächendiagramm. |
| Area3D | `3` | 3D-Flächendiagramm. |
| Area3DStacked | `4` | Gestapeltes 3D-Flächendiagramm. |
| Area3DPercentStacked | `5` | 3D 100 % gestapeltes Flächendiagramm. |
| Bar | `6` | Balkendiagramm. |
| BarStacked | `7` | Gestapeltes Balkendiagramm. |
| BarPercentStacked | `8` | 100 % gestapeltes Balkendiagramm. |
| Bar3D | `9` | 3D-Balkendiagramm. |
| Bar3DStacked | `10` | Gestapeltes 3D-Balkendiagramm. |
| Bar3DPercentStacked | `11` | 3D 100 % gestapeltes Balkendiagramm. |
| Bubble | `12` | Blasendiagramm. |
| Bubble3D | `13` | 3D-Blasendiagramm. |
| Column | `14` | Säulendiagramm. |
| ColumnStacked | `15` | Gestapeltes Säulendiagramm. |
| ColumnPercentStacked | `16` | 100 % gestapeltes Säulendiagramm. |
| Column3D | `17` | 3D-Säulendiagramm. |
| Column3DStacked | `18` | Gestapeltes 3D-Säulendiagramm. |
| Column3DPercentStacked | `19` | 3D 100 % gestapeltes Säulendiagramm. |
| Column3DClustered | `20` | 3D-Säulendiagramm mit Clustern. |
| Doughnut | `21` | Ringdiagramm. |
| Line | `22` | Liniendiagramm. |
| LineStacked | `23` | Gestapeltes Liniendiagramm. |
| LinePercentStacked | `24` | 100 % gestapeltes Liniendiagramm. |
| Line3D | `25` | 3D-Liniendiagramm. |
| Pie | `26` | Kreisdiagramm. |
| Pie3D | `27` | 3D-Kreisdiagramm. |
| PieOfBar | `28` | Kreis- oder Balkendiagramm. |
| PieOfPie | `29` | Kreisdiagramm. |
| Radar | `30` | Radarkarte. |
| Scatter | `31` | Streudiagramm. |
| Stock | `32` | Aktienchart. |
| Surface | `33` | Oberflächenkarte. |
| Surface3D | `34` | 3D-Oberflächendiagramm. |
| Treemap | `35` | Treemap-Diagramm. |
| Sunburst | `36` | Sunburst-Diagramm. |
| Histogram | `37` | Histogrammdiagramm. |
| Pareto | `38` | Pareto-Diagramm. |
| BoxAndWhisker | `39` | Box-and-Whisker-Diagramm. |
| Waterfall | `40` | Wasserfalldiagramm. |
| Funnel | `41` | Trichterdiagramm. |

## Beispiele

Zeigt, wie ein geeigneter Diagrammreihentyp für einen Diagrammtyp erstellt wird.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Es gibt mehrere Möglichkeiten, die Seriensammlung eines Diagramms zu füllen.
    // Für unterschiedliche Diagrammtypen sind unterschiedliche Reihenschemata vorgesehen.
    // 1 – Säulendiagramm mit Säulen, die entlang der X-Achse nach Kategorie gruppiert und in Bänder eingeteilt sind:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Fügen Sie zwei Dezimalwertreihen ein, die für jede jeweilige Kategorie einen Wert enthalten.
    // Dieses Säulendiagramm besteht aus drei Gruppen mit jeweils zwei Säulen.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Kategorien werden entlang der X-Achse verteilt und Werte entlang der Y-Achse.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Flächendiagramm mit entlang der X-Achse verteilten Daten:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Fügt eine Reihe mit einem Dezimalwert für jedes jeweilige Datum ein.
    // Die Daten werden entlang einer linearen X-Achse verteilt,
    // und die dieser Reihe hinzugefügten Werte erstellen Datenpunkte.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D-Streudiagramm:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Jede Reihe benötigt zwei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte und das zweite die entsprechenden Y-Werte
    // von Datenpunkten im Diagrammgraphen.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Blasendiagramm:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Jede Reihe benötigt drei Dezimalarrays gleicher Länge.
    // Das erste Array enthält X-Werte, das zweite enthält die entsprechenden Y-Werte,
    // und der dritte enthält Durchmesser für jeden Datenpunkt des Diagramms.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Fügen Sie mithilfe eines Dokumentgenerators mit einem angegebenen Diagrammtyp, einer angegebenen Breite und Höhe ein Diagramm ein und entfernen Sie die Demodaten.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
