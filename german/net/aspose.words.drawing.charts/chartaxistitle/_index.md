---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words für .NET
description: Erkunden Sie die Klasse Aspose.Words.ChartAxisTitle, um Achsentiteleigenschaften einfach zu verwalten und die visuelle Wirkung Ihres Dokuments zu verbessern.
type: docs
weight: 910
url: /de/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Bietet Zugriff auf die Achsentiteleigenschaften.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit -Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartAxisTitle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Bietet Zugriff auf die Schriftformatierung des Achsentitels. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung des Achsentitels. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente den Titel überlappen dürfen. Der Standardwert ist`FALSCH` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Bestimmt, ob der Titel für die Achse angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Liest oder setzt den Text des Achsentitels. Wenn`null` oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt. |

## Beispiele

Zeigt, wie der Achsentitel eines Diagramms festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
