---
title: Class ChartAxis
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartAxis classe. Rappresenta le opzioni degli assi del grafico.
type: docs
weight: 630
url: /it/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Rappresenta le opzioni degli assi del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartAxis
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Ottiene o imposta un flag che indica se l'asse dei valori attraversa l'asse delle categorie tra le categorie. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Restituisce o imposta l'unità di tempo più piccola rappresentata sull'asse delle categorie temporali. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Ottiene o imposta il tipo dell'asse delle categorie. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Specifica come questo asse incrocia l'asse perpendicolare. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Specifica il punto in cui l'asse si incrocia sull'asse perpendicolare. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Definisce il valore di scala delle unità di visualizzazione per l'asse dei valori. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Restituisce il documento a cui appartiene il titolare. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Ottiene o imposta un flag che indica se l'asse ha griglie principali. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Ottiene o imposta un flag che indica se l'asse presenta griglie minori. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Ottiene o imposta un flag che indica se questo asse è nascosto o meno. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Restituisce o imposta i segni di graduazione principali. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Restituisce o imposta la distanza tra i segni di graduazione principali. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Ottiene o imposta un flag che indica se deve essere utilizzata la distanza predefinita tra i segni di graduazione principali. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Restituisce o imposta il valore di scala per i segni di graduazione principali sull'asse delle categorie temporali. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Restituisce o imposta i segni di graduazione minori per l'asse. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Restituisce o imposta la distanza tra i segni di graduazione minori. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Ottiene o imposta un flag che indica se deve essere utilizzata la distanza predefinita tra i segni di graduazione minori. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Restituisce o imposta il valore di scala per i segni di graduazione minori sull'asse delle categorie temporali. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Restituisce a[`ChartNumberFormat`](../chartnumberformat/) oggetto che consente di definire i formati numerici per l'asse. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Restituisce o imposta un flag che indica se i valori dell'asse devono essere visualizzati in ordine inverso, ovvero dal massimo al minimo. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Fornisce l'accesso alle opzioni di scala dell'asse. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Ottiene o imposta l'allineamento del testo delle etichette dei segni di spunta degli assi. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Ottiene o imposta la distanza delle etichette dall'asse. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Restituisce o imposta la posizione delle etichette dei tick sull'asse. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Ottiene o imposta l'intervallo in cui vengono disegnate le etichette dei segni di spunta. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Ottiene o imposta un flag che indica se deve essere utilizzato l'intervallo automatico di disegno delle etichette di graduazione. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Ottiene o imposta l'intervallo in cui vengono disegnati i segni di graduazione. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Fornisce l'accesso alle proprietà del titolo dell'asse. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Restituisce il tipo dell'asse. |

### Esempi

Mostra come inserire un grafico e modificare l'aspetto dei suoi assi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Cancella le serie di dati dimostrativi del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Inserisci una serie di grafici con categorie per l'asse X e rispettivi valori numerici per l'asse Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Gli assi del grafico hanno varie opzioni che possono cambiarne l'aspetto,
// come la direzione, i segni di graduazione delle unità maggiori/minori e i segni di graduazione.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// I grafici a colonne non hanno un asse Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


