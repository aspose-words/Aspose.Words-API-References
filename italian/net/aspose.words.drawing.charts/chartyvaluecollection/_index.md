---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartYValueCollection, la soluzione ideale per gestire in modo efficiente ed efficace i valori Y nelle serie di grafici.
type: docs
weight: 1200
url: /it/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

Rappresenta una raccolta di valori Y per una serie di grafici.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Ottiene il numero di elementi in questa raccolta. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | Ottiene o imposta il codice di formato applicato ai valori Y. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Ottiene o imposta il valore Y all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Restituisce un oggetto enumeratore. |

## Osservazioni

Tutti gli articoli della collezione tranne**null** deve avere lo stesso[`ValueType`](../chartyvalue/valuetype/).

La raccolta consente solo la modifica dei valori Y. Per aggiungere o inserire nuovi valori a una serie di grafici, o rimuovere valori, i metodi appropriati del[`ChartSeries`](../chartseries/) è possibile utilizzare la classe.

## Esempi

Mostra come ottenere dati di serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Cancella il formato individuale di tutti i punti dati.
    // Nei grafici a colonne, i punti dati e i valori dei dati sono uno a uno.
    series.DataPoints[i].ClearFormat();

    // Ottieni il valore Y.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Cambia i colori dei valori massimo e minimo.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Guarda anche

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
