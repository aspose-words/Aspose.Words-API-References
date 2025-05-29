---
title: ChartAxis.BaseTimeUnit
linktitle: BaseTimeUnit
articleTitle: BaseTimeUnit
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartAxis BaseTimeUnit-Eigenschaft, um einfach die kleinste Zeiteinheit auf Ihrer Zeitkategorieachse zu definieren und so die Datenvisualisierung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartaxis/basetimeunit/
---
## ChartAxis.BaseTimeUnit property

Gibt die kleinste Zeiteinheit zurück, die auf der Zeitkategorieachse dargestellt wird, oder legt sie fest.

```csharp
public AxisTimeUnit BaseTimeUnit { get; set; }
```

## Bemerkungen

Die Eigenschaft wirkt sich nur auf Zeitkategorieachsen aus.

## Beispiele

Zeigt, wie ein Diagramm mit Datums-/Uhrzeitwerten eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine benutzerdefinierte Reihe hinzu, die Datums-/Uhrzeitwerte für die X-Achse und entsprechende Dezimalwerte für die Y-Achse enthält.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Untere und obere Grenzen für die X-Achse festlegen.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Stellen Sie die Haupteinheiten der X-Achse auf eine Woche und die Nebeneinheiten auf einen Tag ein.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Definieren Sie die Eigenschaften der Y-Achse für Dezimalwerte.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Siehe auch

* enum [AxisTimeUnit](../../axistimeunit/)
* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
