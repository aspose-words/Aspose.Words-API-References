---
title: ChartDataTable.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font di ChartDataTable per migliorare l'aspetto della tua tabella dati con una formattazione del carattere personalizzabile per una migliore leggibilità e impatto.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartdatatable/font/
---
## ChartDataTable.Font property

Fornisce accesso alla formattazione del carattere della tabella dati.

```csharp
public Font Font { get; }
```

## Esempi

Mostra come visualizzare una tabella dati con dati di serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Guarda anche

* class [Font](../../../aspose.words/font/)
* class [ChartDataTable](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
