---
title: ChartAxisTitle.Text
second_title: Aspose.Words für .NET-API-Referenz
description: ChartAxisTitle eigendom. Ruft den Text des Achsentitels ab oder legt ihn fest. WennNull oder ein leerer Wert angegeben wird wird der automatisch generierte Titel angezeigt.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Ruft den Text des Achsentitels ab oder legt ihn fest. Wenn`Null` oder ein leerer Wert angegeben wird, wird der automatisch generierte Titel angezeigt.

```csharp
public string Text { get; set; }
```

### Bemerkungen

Verwenden[`Show`](../show/) Option, wenn Sie den Titel anzeigen müssen.

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

* class [ChartAxisTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* Montage [Aspose.Words](../../../)


