---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ChartSeriesGroupCollection, Ihre Lösung zum mühelosen Verwalten und Organisieren von ChartSeriesGroup-Objekten.
type: docs
weight: 1100
url: /de/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Stellt eine Sammlung von[`ChartSeriesGroup`](../chartseriesgroup/) Objekte.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Gibt die Anzahl der Seriengruppen in dieser Sammlung zurück. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Gibt einen[`ChartSeriesGroup`](../chartseriesgroup/) am angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Fügt dieser Sammlung eine neue Seriengruppe des angegebenen Serientyps hinzu. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Entfernt eine Seriengruppe am angegebenen Index. Alle untergeordneten Serien werden aus dem Diagramm entfernt. |

## Bemerkungen

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
