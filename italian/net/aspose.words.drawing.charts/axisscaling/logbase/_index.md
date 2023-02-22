---
title: AxisScaling.LogBase
second_title: Aspose.Words per .NET API Reference
description: AxisScaling proprietà. Ottiene o imposta la base logaritmica per un asse logaritmico.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Ottiene o imposta la base logaritmica per un asse logaritmico.

```csharp
public double LogBase { get; set; }
```

### Osservazioni

La proprietà non è supportata dai nuovi grafici di MS Office 2016.

L'intervallo valido di un valore in virgola mobile è maggiore o uguale a 2 e minore o uguale a 1000. La proprietà ha effetto solo se[`Type`](../type/) è impostato su Logarithmic.

L'impostazione di questa proprietà imposta il[`Type`](../type/) proprietà aLogarithmic .

### Esempi

Mostra come applicare il ridimensionamento logaritmico a un asse del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Inserisce una serie con coordinate X/Y per cinque punti.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Il ridimensionamento dell'asse X è lineare per impostazione predefinita,
// visualizzazione di valori incrementali in modo uniforme che coprono il nostro intervallo di valori X (0, 1, 2, 3...).
// Un asse lineare non è l'ideale per i nostri valori Y
// poiché i punti con i valori Y più piccoli saranno più difficili da leggere.
// Una scala logaritmica con base 20 (1, 20, 400, 8000...)
// diffonderà i punti tracciati, permettendoci di leggere più facilmente i loro valori sul grafico.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Guarda anche

* class [AxisScaling](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../axisscaling/)
* assemblea [Aspose.Words](../../../)


