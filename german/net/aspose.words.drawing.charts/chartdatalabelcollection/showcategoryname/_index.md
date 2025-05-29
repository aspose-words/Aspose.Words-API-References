---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft ShowCategoryName in ChartDataLabelCollection. Steuern Sie die Sichtbarkeit der Datenbeschriftungen für Ihre Serien und verbessern Sie die Übersichtlichkeit Ihres Diagramms!
type: docs
weight: 110
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowCategoryName { get; set; }
```

## Bemerkungen

Der für diese Eigenschaft definierte Wert kann für ein einzelnes Datenlabel mit dem überschrieben werden.[`ShowCategoryName`](../../chartdatalabel/showcategoryname/) Eigenschaft.

## Beispiele

Zeigt, wie mit Datenbeschriftungen eines Blasendiagramms gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

    // Fügen Sie eine benutzerdefinierte Reihe mit X/Y-Koordinaten und Durchmesser jeder einzelnen Blase hinzu.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Datenbeschriftungen aktivieren und dann deren Erscheinungsbild ändern.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

### Siehe auch

* class [ChartDataLabelCollection](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
