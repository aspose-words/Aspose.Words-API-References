---
title: ChartAxisType Enum
linktitle: ChartAxisType
articleTitle: ChartAxisType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.Charts.ChartAxisType, um Diagrammachsentypen einfach zu definieren und die Datenvisualisierung Ihres Dokuments zu verbessern.
type: docs
weight: 920
url: /de/net/aspose.words.drawing.charts/chartaxistype/
---
## ChartAxisType enumeration

Gibt den Typ der Diagrammachse an.

```csharp
public enum ChartAxisType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Category | `0` | Kategorieachse eines Diagramms. |
| Series | `1` | Serienachse eines Diagramms. |
| Value | `2` | Werteachse eines Diagramms. |

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
