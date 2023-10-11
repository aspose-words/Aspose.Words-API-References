---
title: ChartAxis.TickLabelSpacingIsAuto
second_title: Aspose.Words für .NET-API-Referenz
description: ChartAxis eigendom. Ruft ein Flag ab oder setzt es das angibt ob das automatische Intervall zum Zeichnen von Teilstrichbeschriftungen verwendet werden soll.
type: docs
weight: 260
url: /de/net/aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/
---
## ChartAxis.TickLabelSpacingIsAuto property

Ruft ein Flag ab oder setzt es, das angibt, ob das automatische Intervall zum Zeichnen von Teilstrichbeschriftungen verwendet werden soll.

```csharp
public bool TickLabelSpacingIsAuto { get; set; }
```

### Bemerkungen

Der Standardwert ist`WAHR`.

Die Eigenschaft wirkt sich auf Textkategorie- und Serienachsen aus. Es wird von den neuen Diagrammen von MS Office 2016 nicht unterstützt.

### Beispiele

Zeigt, wie man ein Diagramm einfügt und das Erscheinungsbild seiner Achsen ändert.

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
// wie ihre Richtung, Dur-/Moll-Einheitenstriche und Teilstriche.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Säulendiagramme haben keine Z-Achse.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Siehe auch

* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartaxis/)
* Montage [Aspose.Words](../../../)


