---
title: AxisBound.Value
second_title: Aspose.Words per .NET API Reference
description: AxisBound proprietà. Restituisce il valore numerico del limite dellasse.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/axisbound/value/
---
## AxisBound.Value property

Restituisce il valore numerico del limite dell'asse.

```csharp
public double Value { get; }
```

### Esempi

Mostra come impostare i limiti degli assi personalizzati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Cancella le serie di dati dimostrativi del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiunge una serie con due array decimali. Il primo array contiene i valori X,
// e il secondo contiene i valori Y corrispondenti per i punti nel grafico a dispersione.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Per impostazione predefinita, il ridimensionamento predefinito viene applicato agli assi X e Y del grafico,
// in modo che entrambi gli intervalli siano sufficientemente grandi da comprendere ogni valore X e Y di ogni serie.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Possiamo definire i limiti dei nostri assi.
// In questo caso, faremo in modo che i righelli dell'asse X e Y mostrino un intervallo compreso tra 0 e 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Crea un grafico a linee con una serie che richiede un intervallo di date sull'asse X e valori decimali per l'asse Y.
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

// Possiamo impostare i limiti degli assi anche sotto forma di date, limitando il grafico a un periodo.
// Impostando l'intervallo su 1980-1990 verranno omessi i due valori della serie
// che sono fuori dall'intervallo del grafico.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Guarda anche

* class [AxisBound](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../axisbound/)
* assemblea [Aspose.Words](../../../)


