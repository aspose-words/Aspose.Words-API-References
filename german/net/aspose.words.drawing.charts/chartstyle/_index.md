---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words für .NET
description: Wenden Sie vordefinierte Diagrammstile in Aspose.Words an. Verbessern Sie die Visualisierung mit ChartStyle-Enumerationen für professionelle Dokumentformatierung.
type: docs
weight: 1130
url: /de/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Gibt vordefinierte Stile eines Diagramms an.

```csharp
public enum ChartStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | `0` | Stellt den Standarddiagrammstil dar. |
| Muted | `1` | Ein Stil mit gedeckten Farben. |
| Saturated | `2` | Ein Stil mit gesättigteren Farben. |
| Shaded | `3` | Ein Stil mit schattierten Datenpunkten. |
| Flat | `4` | Ein Stil mit flachen Datenpunkten ohne Farbverlauf. |
| Shadowed | `5` | Ein Stil mit Datenpunkten, die einen Schatten haben. |
| Gradient | `6` | Ein Stil mit Verlaufsfüllung der Datenpunkte. |
| Original | `7` | Ein Stil mit dem ursprünglichen Erscheinungsbild eines Diagramms. |
| Transparent1 | `8` | Ein Stil mit transparenten Datenpunkten. |
| Transparent2 | `9` | Ein Stil mit transparenten Datenpunkten. |
| Outline | `10` | Ein Stil mit Datenpunkten ohne Füllung, sondern nur mit einem Umriss. |
| OutlineBlack | `11` | Ein Stil mit schwarzem Diagrammhintergrund, bei dem Datenpunkte keine Füllung, sondern nur einen Umriss haben. |
| Black | `12` | Ein Stil mit schwarzem Diagrammhintergrund. |
| Grey | `13` | Ein Stil mit grauem Verlaufsdiagrammhintergrund. |
| Blue | `14` | Ein Stil mit blauem Diagrammhintergrund. |
| ShadedPlot | `15` | Ein Stil, bei dem der Plotbereich schattiert ist. |

## Beispiele

Zeigt, wie der Diagrammstil festgelegt und abgerufen wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Diagramm im Stil „Black“ ein.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Holen Sie sich ein zu aktualisierendes Diagramm.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Holen Sie sich den Diagrammstil.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
