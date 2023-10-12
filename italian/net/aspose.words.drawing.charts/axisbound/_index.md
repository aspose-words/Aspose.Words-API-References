---
title: Class AxisBound
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.AxisBound classe. Rappresenta il limite minimo o massimo dei valori degli assi.
type: docs
weight: 510
url: /it/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Rappresenta il limite minimo o massimo dei valori degli assi.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public sealed class AxisBound
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Crea una nuova istanza che indica che il limite dell'asse deve essere determinato automaticamente da un'applicazione di elaborazione testi . |
| [AxisBound](axisbound/#constructor_2)(DateTime) | Crea un limite dell'asse rappresentato come valore data/ora. |
| [AxisBound](axisbound/#constructor_1)(double) | Crea un limite dell'asse rappresentato come un numero. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Restituisce un flag che indica che il limite dell'asse deve essere determinato automaticamente. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Restituisce il valore numerico del limite dell'asse. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Restituisce il valore del limite dell'asse rappresentato come datetime. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(object) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Serve come funzione hash per questo tipo. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Restituisce una stringa intuitiva che visualizza il valore di questo oggetto. |

### Osservazioni

Il limite può essere specificato come valore numerico, data/ora o speciale "automatico".

Le istanze di questa classe sono immutabili.

### Esempi

Mostra come inserire un grafico con valori di data/ora.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Cancella le serie di dati dimostrativi del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiunge una serie personalizzata contenente valori di data/ora per l'asse X e rispettivi valori decimali per l'asse Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Imposta i limiti inferiore e superiore per l'asse X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Imposta le unità principali dell'asse X su una settimana e le unità minori su un giorno.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Definisce le proprietà dell'asse Y per i valori decimali.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


