---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartDataTable per personalizzare facilmente le tabelle dei dati dei grafici e migliorare la visualizzazione dei dati con potenti funzionalità.
type: docs
weight: 990
url: /it/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Consente di specificare le proprietà di una tabella dati del grafico.

```csharp
public class ChartDataTable
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Fornisce accesso alla formattazione del carattere della tabella dati. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Fornisce accesso al riempimento dello sfondo del testo e alla formattazione del bordo della tabella dati. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Ottiene o imposta un flag che indica se viene visualizzato un bordo orizzontale della tabella dati. Il valore predefinito è`VERO` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Ottiene o imposta un flag che indica se le chiavi della legenda vengono visualizzate nella tabella dati. Il valore predefinito è`VERO` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Ottiene o imposta un flag che indica se viene visualizzato un bordo di contorno, ovvero un bordo attorno ai nomi di serie e categorie, . Il valore predefinito è `VERO` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Ottiene o imposta un flag che indica se viene visualizzato un bordo verticale della tabella dati. Il valore predefinito è`VERO` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Ottiene o imposta un flag che indica se la tabella dati verrà visualizzata per il grafico. Il valore predefinito è `falso` . |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
