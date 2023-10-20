---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.Charts.ChartYValueCollection classe. Rappresenta una raccolta di valori Y per una serie di grafici in C#.
type: docs
weight: 880
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
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Ottiene o imposta il valore Y in corrispondenza dell'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Restituisce un oggetto enumeratore. |

## Osservazioni

Tutti gli articoli della collezione diversi da**nullo** deve avere lo stesso[`ValueType`](../chartyvalue/valuetype/).

La raccolta consente solo di modificare i valori Y. Per aggiungere o inserire nuovi valori in una serie di grafici o rimuovere valori, i metodi appropriati di[`ChartSeries`](../chartseries/) è possibile utilizzare la classe.

## Esempi

Mostra come ottenere i dati delle serie di grafici.

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
    // I punti dati e i valori dei dati sono uno a uno nei grafici a colonne.
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
