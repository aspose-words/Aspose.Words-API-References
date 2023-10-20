---
title: AxisCrosses Enum
linktitle: AxisCrosses
articleTitle: AxisCrosses
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Charts.AxisCrosses opsomming. Gibt die möglichen Kreuzungspunkte für eine Achse an in C#.
type: docs
weight: 540
url: /de/net/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enumeration

Gibt die möglichen Kreuzungspunkte für eine Achse an.

```csharp
public enum AxisCrosses
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Automatic | `0` | Die Kategorieachse schneidet sich am Nullpunkt der Werteachse (falls möglich) oder am Minimalwert , wenn das Minimum größer als Null ist, oder am Maximum, wenn das Maximum kleiner als Null ist. |
| Maximum | `1` | Eine senkrechte Achse kreuzt sich beim Maximalwert der Achse. |
| Minimum | `2` | Eine senkrechte Achse schneidet sich am Minimalwert der Achse. |
| Custom | `3` | Eine senkrechte Achse schneidet sich am angegebenen Wert der Achse. |

## Beispiele

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
