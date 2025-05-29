---
title: AxisBound.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words per .NET
description: Scopri il valore di AxisBound. Recupera facilmente i limiti numerici degli assi per una visualizzazione precisa dei dati e approfondimenti analitici avanzati.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/axisbound/value/
---
## AxisBound.Value property

Restituisce il valore numerico del limite dell'asse.

```csharp
public double Value { get; }
```

## Esempi

Mostra come impostare limiti personalizzati degli assi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiungi una serie con due array decimali. Il primo array contiene i valori X,
// e il secondo contiene i valori Y corrispondenti per i punti nel grafico a dispersione.
chart.Series.Add("Series 1",
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 },
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Per impostazione predefinita, la scala predefinita viene applicata agli assi X e Y del grafico,
// in modo che entrambi i loro intervalli siano sufficientemente grandi da comprendere ogni valore X e Y di ogni serie.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Possiamo definire i limiti dei nostri assi.
// In questo caso, faremo in modo che entrambi i righelli dell'asse X e Y mostrino un intervallo da 0 a 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Crea un grafico a linee con una serie che richiede un intervallo di date sull'asse X e valori decimali sull'asse Y.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// Possiamo anche impostare i limiti degli assi sotto forma di date, limitando il grafico a un periodo.
// Impostando l'intervallo su 1980-1990 verranno omessi due valori della serie
// che sono al di fuori dell'intervallo del grafico.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Guarda anche

* class [AxisBound](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
