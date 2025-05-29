---
title: ChartSeriesGroup.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words für .NET
description: Entdecken Sie die SeriesType-Eigenschaft von ChartSeriesGroup, um Diagrammreihentypen in Ihren Datenvisualisierungen einfach zu identifizieren und so Analysen und Erkenntnisse zu verbessern.
type: docs
weight: 110
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/seriestype/
---
## ChartSeriesGroup.SeriesType property

Ruft den Typ der in dieser Gruppe enthaltenen Diagrammreihe ab.

```csharp
public ChartSeriesType SeriesType { get; }
```

## Beispiele

Zeigt, wie mit der sekundären Achse des Diagramms gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Standardmäßig generierte Serien löschen.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Erstellen Sie eine zusätzliche Seriengruppe, ebenfalls vom Typ Linie.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Geben Sie die Verwendung sekundärer Achsen für die neue Seriengruppe an.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Sekundäre X-Achse ausblenden.
newSeriesGroup.AxisX.Hidden = true;
// Titel der sekundären Y-Achse definieren.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Fügen Sie der neuen Seriengruppe eine Serie hinzu.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Siehe auch

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroup](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
