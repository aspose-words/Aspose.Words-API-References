---
title: ChartSeries.BubbleSizes
linktitle: BubbleSizes
articleTitle: BubbleSizes
second_title: Aspose.Words für .NET
description: Entdecken Sie die BubbleSizes-Eigenschaft von ChartSeries, um auf anpassbare Blasengrößen zuzugreifen und so Ihre Datenvisualisierung und Diagrammerstellung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartseries/bubblesizes/
---
## ChartSeries.BubbleSizes property

Ruft eine Sammlung von Blasengrößen für diese Diagrammreihe ab.

```csharp
public BubbleSizeCollection BubbleSizes { get; }
```

## Beispiele

Zeigt, wie mit dem Formatcode der Diagrammdaten gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Blasendiagramm ein.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Datenformatcodes festlegen.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Siehe auch

* class [BubbleSizeCollection](../../bubblesizecollection/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
