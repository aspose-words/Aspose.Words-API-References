---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsHidden-Eigenschaft von ChartLegendEntry und steuern Sie mühelos die Sichtbarkeit der Diagrammlegende. Verbessern Sie Ihre Datenpräsentation mit dieser einfachen Umschaltfunktion!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. Der Standardwert ist**FALSCH** .

```csharp
public bool IsHidden { get; set; }
```

## Bemerkungen

Wenn ein Eintrag in der Diagrammlegende ausgeblendet wird, hat dies keine Auswirkungen auf die entsprechende Diagrammreihe oder Trendlinie, die weiterhin im Diagramm angezeigt wird.

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

* class [ChartLegendEntry](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
