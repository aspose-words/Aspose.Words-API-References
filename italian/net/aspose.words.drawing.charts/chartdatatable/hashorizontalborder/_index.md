---
title: ChartDataTable.HasHorizontalBorder
linktitle: HasHorizontalBorder
articleTitle: HasHorizontalBorder
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartDataTable HasHorizontalBorder per personalizzare facilmente l'aspetto della tua tabella dati. Controlla i bordi orizzontali per una maggiore chiarezza visiva!
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartdatatable/hashorizontalborder/
---
## ChartDataTable.HasHorizontalBorder property

Ottiene o imposta un flag che indica se viene visualizzato un bordo orizzontale della tabella dati. Il valore predefinito è`VERO` .

```csharp
public bool HasHorizontalBorder { get; set; }
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

* class [ChartDataTable](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
