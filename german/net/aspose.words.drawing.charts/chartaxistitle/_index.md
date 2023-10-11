---
title: Class ChartAxisTitle
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartAxisTitle klas. Bietet Zugriff auf die Eigenschaften des Achsentitels.
type: docs
weight: 650
url: /de/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Bietet Zugriff auf die Eigenschaften des Achsentitels.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartAxisTitle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente den Titel überlappen dürfen. Der Standardwert ist`FALSCH` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Legt fest, ob der Titel für die Achse angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Ruft den Text des Achsentitels ab oder legt ihn fest. Wenn`Null` oder ein leerer Wert angegeben wird, wird der automatisch generierte Titel angezeigt. |

### Beispiele

Zeigt, wie der Titel der Diagrammachse festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Achsentitel festlegen.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


