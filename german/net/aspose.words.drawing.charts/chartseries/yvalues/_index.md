---
title: ChartSeries.YValues
linktitle: YValues
articleTitle: YValues
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartSeries YValues-Eigenschaft, um auf eine leistungsstarke Sammlung von Y-Werten zuzugreifen und so Ihre Möglichkeiten zur Datenvisualisierung und -analyse zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words.drawing.charts/chartseries/yvalues/
---
## ChartSeries.YValues property

Ruft eine Sammlung von Y-Werten für diese Diagrammreihe ab.

```csharp
public ChartYValueCollection YValues { get; }
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

* class [ChartYValueCollection](../../chartyvaluecollection/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
