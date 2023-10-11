---
title: Enum AxisBuiltInUnit
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.AxisBuiltInUnit opsomming. Gibt die Anzeigeeinheiten für eine Achse an.
type: docs
weight: 520
url: /de/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

Gibt die Anzeigeeinheiten für eine Achse an.

```csharp
public enum AxisBuiltInUnit
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Gibt an, dass die Werte im Diagramm so angezeigt werden sollen, wie sie sind. |
| Custom | `1` | Gibt an, dass die Werte im Diagramm durch einen benutzerdefinierten Divisor geteilt werden sollen. Dieser Wert wird von den neuen Diagrammtypen von MS Office 2016 nicht unterstützt |
| Billions | `2` | Gibt an, dass die Werte im Diagramm durch 1.000.000.000 geteilt werden sollen. |
| HundredMillions | `3` | Gibt an, dass die Werte im Diagramm durch 100.000.000 geteilt werden sollen. |
| Hundreds | `4` | Gibt an, dass die Werte im Diagramm durch 100 geteilt werden sollen. |
| HundredThousands | `5` | Gibt an, dass die Werte im Diagramm durch 100.000 geteilt werden sollen. |
| Millions | `6` | Gibt an, dass die Werte im Diagramm durch 1.000.000 geteilt werden sollen. |
| TenMillions | `7` | Gibt an, dass die Werte im Diagramm durch 10.000.000 geteilt werden sollen. |
| TenThousands | `8` | Gibt an, dass die Werte im Diagramm durch 10.000 geteilt werden sollen. |
| Thousands | `9` | Gibt an, dass die Werte im Diagramm durch 1.000 geteilt werden sollen. |
| Trillions | `10` | Gibt an, dass die Werte im Diagramm durch 1.000.000.000.0000 geteilt werden sollen. |
| Percentage | `11` | Gibt an, dass die Werte im Diagramm durch 0,01 geteilt werden sollen. Dieser Wert wird nur von den neuen Diagrammtypen von MS Office 2016 unterstützt. |

### Beispiele

Zeigt, wie die Teilstriche und angezeigten Werte einer Diagrammachse manipuliert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Setzen Sie die kleinen Teilstriche der Y-Achse so, dass sie vom Plotbereich weg zeigen.
// und die großen Markierungen, um die Achse zu kreuzen.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Stellen Sie die Y-Achse so ein, dass alle 10 Einheiten ein großer Tick und alle 1 Einheit ein kleiner Tick angezeigt wird.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Setze die Grenzen der Y-Achse auf -10 und 20.
// Auf dieser Y-Achse werden nun 4 große Teilstriche und 27 kleine Teilstriche angezeigt.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Setzen Sie für die X-Achse alle 10 Einheiten die Hauptteilstriche.
// jeder kleine Teilstrich bei 2,5 Einheiten.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Konfigurieren Sie beide Arten von Teilstrichen so, dass sie im Diagrammbereich angezeigt werden.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Legen Sie die Grenzen der X-Achse so fest, dass die X-Achse 5 große Teilstriche und 12 kleine Teilstriche umfasst.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Stellen Sie die Tick-Beschriftungen so ein, dass ihr Wert in Millionen angezeigt wird.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Wir können einen spezifischeren Wert festlegen, anhand dessen Tick-Beschriftungen ihre Werte anzeigen.
// Diese Anweisung entspricht der obigen.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


