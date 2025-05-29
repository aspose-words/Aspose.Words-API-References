---
title: ChartDataLabel.LeftMode
linktitle: LeftMode
articleTitle: LeftMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartDataLabel LeftMode per personalizzare il posizionamento delle etichette dati nei tuoi grafici. Migliora la chiarezza e la presentazione con un controllo preciso.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chartdatalabel/leftmode/
---
## ChartDataLabel.LeftMode property

Ottiene o imposta la modalità di interpretazione del[`Left`](../left/) valore della proprietà: se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dal suo[`Position`](../position/) Proprietà .

```csharp
public ChartDataLabelLocationMode LeftMode { get; set; }
```

## Osservazioni

La proprietà non può essere impostata in un grafico di Word 2016.

## Esempi

Mostra come posizionare le etichette dei dati del grafico a ciambella all'esterno della ciambella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Elimina la serie generata di default.
seriesColl.Clear();

// Nascondi la legenda.
chart.Legend.Position = LegendPosition.None;

// Genera dati.
const int dataLength = 20;
double totalValue = 0;
string[] categories = new string[dataLength];
double[] values = new double[dataLength];

for (int i = 0; i < dataLength; i++)
{
    categories[i] = $"Category {i}";
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

ChartSeries series = seriesColl.Add("Series 1", categories, values);
series.HasDataLabels = true;

ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.ShowLeaderLines = true;

// La proprietà Posizione non può essere utilizzata per i grafici a ciambella. Posizioniamo le etichette dati utilizzando le proprietà Sinistra e In alto.
// proprietà attorno a un cerchio esterno alla ciambella del grafico.
// L'origine si trova nell'angolo in alto a sinistra del grafico.

const double titleAreaHeight = 25.5; // Questo può essere calcolato utilizzando il testo del titolo e il carattere.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Questo può essere calcolato utilizzando il font dell'etichetta.
const double oneCharLabelWidth = 12.75; // Questo può essere calcolato per ogni etichetta utilizzando il suo testo e il suo carattere.
const double twoCharLabelWidth = 17.25; // Questo può essere calcolato per ogni etichetta utilizzando il suo testo e il suo carattere.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Poiché i punti dati iniziano dall'alto, le coordinate X utilizzate nelle proprietà Sinistra e Superiore di
// le etichette dei dati puntano verso destra e le coordinate Y puntano verso il basso, l'angolo iniziale è -PI/2.
double totalAngle = -System.Math.PI / 2;
ChartDataLabel previousLabel = null;

for (int i = 0; i < series.YValues.Count; i++)
{
    ChartDataLabel dataLabel = dataLabels[i];

    double value = series.YValues[i].DoubleValue;
    double labelWidth;
    if (value < 10)
        labelWidth = oneCharLabelWidth;
    else
        labelWidth = twoCharLabelWidth;
    double labelSegmentAngle = value / totalValue * 2 * System.Math.PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System.Math.Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System.Math.Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // Se l'etichetta dati corrente si sovrappone ad altre etichette, spostarla orizzontalmente.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Spostati a destra in alto, a sinistra in basso.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System.Math.PI);
        int factor;
        if (isOnTop)
            factor = 1;
        else
            factor = -1;

        labelLeft = previousLabel.Left + labelWidth * factor + labelMargin;
    }

    dataLabel.Left = labelLeft;
    dataLabel.LeftMode = ChartDataLabelLocationMode.Absolute;
    dataLabel.Top = labelTop;
    dataLabel.TopMode = ChartDataLabelLocationMode.Absolute;

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc.Save(ArtifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### Guarda anche

* enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* class [ChartDataLabel](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
