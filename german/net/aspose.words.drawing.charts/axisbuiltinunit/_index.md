---
title: Enum AxisBuiltInUnit
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.AxisBuiltInUnit opsomming. Gibt die Anzeigeeinheiten für eine Achse an.
type: docs
weight: 510
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
| None | `0` | Gibt an, dass die Werte im Diagramm unverändert angezeigt werden sollen. |
| Custom | `1` | Gibt an, dass die Werte im Diagramm durch einen benutzerdefinierten Divisor dividiert werden sollen. Dieser Wert wird von den neuen Diagrammtypen von MS Office 2016 nicht unterstützt. |
| Billions | `2` | Gibt an, dass die Werte im Diagramm durch 1.000.000.000 dividiert werden sollen. |
| HundredMillions | `3` | Gibt an, dass die Werte im Diagramm durch 100.000.000 dividiert werden sollen. |
| Hundreds | `4` | Gibt an, dass die Werte im Diagramm durch 100 geteilt werden sollen. |
| HundredThousands | `5` | Gibt an, dass die Werte im Diagramm durch 100.000 dividiert werden sollen. |
| Millions | `6` | Gibt an, dass die Werte im Diagramm durch 1.000.000 geteilt werden sollen. |
| TenMillions | `7` | Gibt an, dass die Werte im Diagramm durch 10.000.000 dividiert werden sollen. |
| TenThousands | `8` | Gibt an, dass die Werte im Diagramm durch 10.000 geteilt werden sollen. |
| Thousands | `9` | Gibt an, dass die Werte im Diagramm durch 1.000 dividiert werden sollen. |
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

// Stellen Sie die kleinen Teilstriche der Y-Achse so ein, dass sie vom Plotbereich weg zeigen,
// und die großen Teilstriche, um die Achse zu kreuzen.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Stellen Sie die Y-Achse so ein, dass alle 10 Einheiten ein großer Tick und alle 1 Einheit ein kleiner Tick angezeigt wird.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Setze die Grenzen der Y-Achse auf -10 und 20.
// Diese Y-Achse zeigt nun 4 große Teilstriche und 27 kleinere Teilstriche an.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Setzen Sie für die X-Achse die Hauptteilstriche alle 10 Einheiten,
// jeder kleinere Teilstrich bei 2,5 Einheiten.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Konfigurieren Sie beide Arten von Teilstrichen so, dass sie innerhalb des Diagrammplotbereichs erscheinen.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Legen Sie die Grenzen der X-Achse so fest, dass die X-Achse 5 große Teilstriche und 12 kleinere Teilstriche umfasst.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Stellen Sie die Tick-Labels so ein, dass ihr Wert in Millionen angezeigt wird.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Wir können einen spezifischeren Wert festlegen, mit dem Tick-Labels ihre Werte anzeigen.
// Diese Anweisung entspricht der obigen.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


