---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.AxisTickLabels, die entwickelt wurde, um die Achsenmarkierungsbeschriftungen Ihres Diagramms mit anpassbaren Eigenschaften für eine bessere Datenvisualisierung zu verbessern.
type: docs
weight: 840
url: /de/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

Stellt Eigenschaften der Beschriftungen der Achsenmarkierungen dar.

```csharp
public class AxisTickLabels
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | Ruft die Textausrichtung der Achsenmarkierungsbeschriftungen ab oder legt diese fest. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | Bietet Zugriff auf die Schriftformatierung der Teilstrichbeschriftungen. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | Ruft ein Flag ab oder legt ein Flag fest, das angibt, ob zum Zeichnen der Teilstrichbeschriftungen ein automatisches Intervall verwendet werden soll. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | Ruft den Abstand der Teilstrichbeschriftungen von der Achse ab oder legt ihn fest. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | Ruft die Ausrichtung des Teilstrichbeschriftungstextes ab oder legt sie fest. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | Ruft die Position der Teilstrichbeschriftungen auf der Achse ab oder legt sie fest. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | Ruft die Drehung der Teilstrichbeschriftungen in Grad ab oder legt sie fest. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | Ruft das Intervall ab oder legt es fest, in dem die Teilstrichbeschriftungen gezeichnet werden. |

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
