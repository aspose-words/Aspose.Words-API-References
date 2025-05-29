---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartSeriesGroup, die die Verwaltung von Diagrammreiheneigenschaften für eine verbesserte Datenvisualisierung und -analyse vereinfacht.
type: docs
weight: 1090
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Stellt Eigenschaften einer Diagrammreihengruppe dar, d. h. die Eigenschaften von Diagrammreihen desselben Typs , die denselben Achsen zugeordnet sind.

```csharp
public class ChartSeriesGroup
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Ruft die Achsengruppe ab oder legt sie fest, zu der diese Seriengruppe gehört. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Bietet Zugriff auf die Eigenschaften der X-Achse dieser Seriengruppe. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Bietet Zugriff auf die Eigenschaften der Y-Achse dieser Seriengruppe. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Ruft die Größe der Blasen als Prozentsatz ihrer Standardgröße ab oder legt sie fest. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Ruft die Lochgröße des übergeordneten Ringdiagramms als Prozentsatz ab oder legt sie fest. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Ruft den Winkel des ersten Segments des übergeordneten Kreisdiagramms in Grad ab oder legt ihn fest. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Ruft den Prozentsatz der Lückenbreite zwischen Diagrammelementen ab oder legt ihn fest. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Ruft den Prozentsatz ab, um den sich die Balken oder Spalten der Serie überlappen, oder legt diesen fest. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Ruft die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz ab oder legt diese fest. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Ruft eine Sammlung von Serien ab, die zu dieser Seriengruppe gehören. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Ruft den Typ der in dieser Gruppe enthaltenen Diagrammreihe ab. |

## Bemerkungen

Kombinationsdiagramme enthalten mehrere Diagrammseriengruppen mit einer separaten Gruppe für jeden Serientyp.

Sie können auch eine Diagrammreihengruppe erstellen, um einer oder mehreren Diagrammreihen sekundäre Achsen zuzuweisen.

Um mehr zu erfahren, besuchen Sie die[ Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
