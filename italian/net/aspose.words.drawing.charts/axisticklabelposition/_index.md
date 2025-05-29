---
title: AxisTickLabelPosition Enum
linktitle: AxisTickLabelPosition
articleTitle: AxisTickLabelPosition
second_title: Aspose.Words per .NET
description: Scopri l'enumerazione Aspose.Words.Drawing.Charts.AxisTickLabelPosition, che definisce il posizionamento ottimale delle etichette di graduazione per una maggiore chiarezza e presentazione dei grafici.
type: docs
weight: 830
url: /it/net/aspose.words.drawing.charts/axisticklabelposition/
---
## AxisTickLabelPosition enumeration

Specifica le possibili posizioni per le etichette di spunta.

```csharp
public enum AxisTickLabelPosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| High | `0` | Specifica che le etichette degli assi devono essere all'estremità superiore dell'asse perpendicolare. |
| Low | `1` | Specifica che le etichette degli assi devono essere all'estremità inferiore dell'asse perpendicolare. |
| NextToAxis | `2` | Specifica che le etichette degli assi devono essere accanto all'asse. |
| None | `3` | Specifica che le etichette degli assi non vengono disegnate. |
| Default | `2` | Specifica il valore predefinito della posizione delle etichette di spunta. |

## Esempi

Mostra come inserire grafici con valori di data/ora.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiungi una serie personalizzata contenente valori di data/ora per l'asse X e rispettivi valori decimali per l'asse Y.
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

// Imposta le unità principali dell'asse X su una settimana e le unità secondarie su un giorno.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Definisci le proprietà dell'asse Y per i valori decimali.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
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
