---
title: AxisTickLabels.Offset
linktitle: Offset
articleTitle: Offset
second_title: Aspose.Words für .NET
description: Passen Sie den AxisTickLabels-Offset an, um den Abstand der Teilstrichbeschriftungen von der Achse anzupassen und so die Übersichtlichkeit und Optik Ihrer Datenvisualisierungen zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/axisticklabels/offset/
---
## AxisTickLabels.Offset property

Ruft den Abstand der Teilstrichbeschriftungen von der Achse ab oder legt ihn fest.

```csharp
public int Offset { get; set; }
```

## Bemerkungen

Die Eigenschaft stellt einen Prozentsatz des Standard-Beschriftungsversatzes dar.

Der gültige Bereich liegt zwischen 0 und 1000 Prozent (einschließlich). Der Standardwert ist 100 %.

Die Eigenschaft wirkt sich nur auf Kategorieachsen aus. Sie wird von den neuen Diagrammen in MS Office 2016 nicht unterstützt.

## Beispiele

Zeigt, wie Sie ein Diagramm einfügen und die Darstellung seiner Achsen ändern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine Diagrammreihe mit Kategorien für die X-Achse und entsprechenden numerischen Werten für die Y-Achse ein.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Diagrammachsen haben verschiedene Optionen, die ihr Aussehen ändern können,
// wie etwa ihre Richtung, große/kleine Einheitsstriche und Teilstriche.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Säulendiagramme haben keine Z-Achse.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Siehe auch

* class [AxisTickLabels](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
