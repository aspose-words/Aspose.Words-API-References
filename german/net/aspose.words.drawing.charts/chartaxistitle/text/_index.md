---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Entdecken Sie die Text-Eigenschaft ChartAxisTitle, um Ihre Achsentitel einfach anzupassen. Legen Sie dynamische Titel fest oder rufen Sie sie für eine verbesserte Datenvisualisierung ab.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Liest oder setzt den Text des Achsentitels. Wenn`null` oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt.

```csharp
public string Text { get; set; }
```

## Bemerkungen

Verwenden[`Show`](../show/)Option, wenn Sie den Titel anzeigen müssen.

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

* class [ChartAxisTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
