---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.ChartDataLabelPosition, um Ihre Diagrammdatenbeschriftungen für bessere Übersichtlichkeit und Präsentation einfach anzupassen.
type: docs
weight: 960
url: /de/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Gibt die Position für eine Diagrammdatenbeschriftung an.

```csharp
public enum ChartDataLabelPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Center | `0` | Gibt an, dass eine Datenbeschriftung zentriert auf einer Datenmarkierung angezeigt werden soll. |
| Left | `1` | Gibt an, dass links von einer Datenmarkierung eine Datenbeschriftung angezeigt werden soll. |
| Right | `2` | Gibt an, dass rechts neben einer Datenmarkierung eine Datenbeschriftung angezeigt werden soll. |
| Above | `3` | Gibt an, dass über einer Datenmarkierung eine Datenbeschriftung angezeigt werden soll. |
| Below | `4` | Gibt an, dass unter einer Datenmarkierung eine Datenbeschriftung angezeigt werden soll. |
| InsideBase | `5` | Gibt an, dass eine Datenbeschriftung innerhalb der Basis einer Datenmarkierung angezeigt werden soll. |
| InsideEnd | `6` | Gibt an, dass am Ende einer Datenmarkierung eine Datenbeschriftung angezeigt werden soll. |
| OutsideEnd | `7` | Gibt an, dass eine Datenbeschriftung außerhalb des Endes einer Datenmarkierung angezeigt werden soll. |
| BestFit | `8` | Gibt an, dass eine Datenbeschriftung an der am besten geeigneten Position angezeigt werden soll. |

## Bemerkungen

Nicht alle Serientypen erlauben die Angabe von Beschriftungspositionen. Und diejenigen, die dies tun, unterstützen nicht alle Werte.

## Beispiele

Zeigt, wie die Position der Datenbeschriftung festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Säulendiagramm einfügen.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

// Serie hinzufügen.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Datenbeschriftungen anzeigen und Schriftfarbe festlegen.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Position der Datenbeschriftung festlegen.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
