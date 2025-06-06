---
title: ChartLegendEntryCollection Class
linktitle: ChartLegendEntryCollection
articleTitle: ChartLegendEntryCollection
second_title: Aspose.Words für .NET
description: Erkunden Sie Aspose.Words.ChartLegendEntryCollection, um Diagrammlegendeneinträge effizient zu verwalten und die visuelle Darstellung Ihrer Dokumente mühelos zu verbessern.
type: docs
weight: 1030
url: /de/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

Stellt eine Sammlung von Diagrammlegendeneinträgen dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | Gibt die Anzahl der[`ChartLegendEntry`](../chartlegendentry/) in dieser Sammlung. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | Rückgaben[`ChartLegendEntry`](../chartlegendentry/) für den angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

## Beispiele

Zeigt, wie mit einem Legendeneintrag für Diagrammreihen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Siehe auch

* class [ChartLegendEntry](../chartlegendentry/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
