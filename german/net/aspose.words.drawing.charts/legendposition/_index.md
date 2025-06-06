---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.Charts.LegendPosition, um die Position Ihrer Diagrammlegende für eine verbesserte Datenvisualisierung einfach anzupassen.
type: docs
weight: 1230
url: /de/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Gibt die möglichen Positionen für eine Diagrammlegende an.

```csharp
public enum LegendPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Für das Diagramm wird keine Legende angezeigt. |
| Bottom | `1` | Gibt an, dass die Legende am unteren Rand des Diagramms angezeigt werden soll. |
| Left | `2` | Gibt an, dass die Legende links vom Diagramm angezeigt werden soll. |
| Right | `3` | Gibt an, dass die Legende rechts vom Diagramm angezeigt werden soll. |
| Top | `4` | Gibt an, dass die Legende oben im Diagramm angezeigt werden soll. |
| TopRight | `5` | Gibt an, dass die Legende oben rechts im Diagramm angezeigt werden soll. |

## Beispiele

Zeigt, wie das Erscheinungsbild der Legende eines Diagramms bearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Verschieben Sie die Legende des Diagramms in die obere rechte Ecke.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Geben Sie anderen Diagrammelementen, beispielsweise dem Graphen, mehr Platz, indem Sie zulassen, dass sie die Legende überlappen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
