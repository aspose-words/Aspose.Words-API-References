---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.ChartFormat-Klasse für erweiterte Diagrammelementgestaltung. Optimieren Sie Ihre Dokumente mit professionellen, anpassbaren Diagrammdesigns.
type: docs
weight: 1000
url: /de/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Stellt die Formatierung eines Diagrammelements dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Ruft die Füllformatierung für das übergeordnete Diagrammelement ab. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Ruft ein Flag ab, das angibt, ob ein Format definiert ist. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Ruft den Formtyp des übergeordneten Diagrammelements ab oder legt ihn fest. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Ruft die Linienformatierung für das übergeordnete Diagrammelement ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Setzt die Füllung des Diagrammelements auf den Standardwert zurück. |

## Beispiele

Zeigt, wie die Diagrammformatierung verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Diagrammhintergrund formatieren.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Achsenmarkierungsbeschriftungen ausblenden.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Diagrammtitel formatieren.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Achsentitel formatieren.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Legende formatieren.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
