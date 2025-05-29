---
title: ChartAxis.MinorTickMark
linktitle: MinorTickMark
articleTitle: MinorTickMark
second_title: Aspose.Words für .NET
description: Passen Sie Ihre ChartAxis mit der MinorTickMark-Eigenschaft an, um die Achsenpräzision zu verbessern und die Datenvisualisierung zu optimieren. Setzen oder geben Sie kleine Teilstriche ganz einfach zurück!
type: docs
weight: 160
url: /de/net/aspose.words.drawing.charts/chartaxis/minortickmark/
---
## ChartAxis.MinorTickMark property

Gibt die kleinen Teilstriche für die Achse zurück oder legt sie fest.

```csharp
public AxisTickMark MinorTickMark { get; set; }
```

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

* enum [AxisTickMark](../../axistickmark/)
* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
