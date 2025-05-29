---
title: ChartAxis.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words für .NET
description: Entdecken Sie die Skalierungseigenschaften von ChartAxis für optimale Achsenanpassungen. Erhalten Sie präzise Kontrolle über Ihre Datenvisualisierung mit benutzerfreundlichen Skalierungsoptionen.
type: docs
weight: 220
url: /de/net/aspose.words.drawing.charts/chartaxis/scaling/
---
## ChartAxis.Scaling property

Bietet Zugriff auf die Skalierungsoptionen der Achse.

```csharp
public AxisScaling Scaling { get; }
```

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

* class [AxisScaling](../../axisscaling/)
* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
