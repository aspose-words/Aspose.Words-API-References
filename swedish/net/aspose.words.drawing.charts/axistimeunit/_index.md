---
title: AxisTimeUnit Enum
linktitle: AxisTimeUnit
articleTitle: AxisTimeUnit
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Charts.AxisTimeUnit uppräkning. Anger tidsenheten för axlar i C#.
type: docs
weight: 600
url: /sv/net/aspose.words.drawing.charts/axistimeunit/
---
## AxisTimeUnit enumeration

Anger tidsenheten för axlar.

```csharp
public enum AxisTimeUnit
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Automatic | `0` | Anger att enheten inte var explicit inställd och standardvärdet ska användas. |
| Days | `1` | Anger att diagramdata ska visas i dagar. |
| Months | `2` | Anger att diagramdata ska visas i månader. |
| Years | `3` | Anger att sjökortsdata ska visas i år. |

## Exempel

Visar hur man infogar diagram med datum/tidsvärden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie som innehåller datum/tid-värden för X-axeln och respektive decimalvärden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Sätt nedre och övre gränser för X-axeln.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Ställ in X-axelns huvudenheter till en vecka och de mindre enheterna till en dag.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Definiera Y-axelegenskaper för decimalvärden.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
