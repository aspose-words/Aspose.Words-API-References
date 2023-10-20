---
title: AxisDisplayUnit.Unit
linktitle: Unit
articleTitle: Unit
second_title: Aspose.Words per .NET
description: AxisDisplayUnit Unit proprietà. Ottiene o imposta il valore di scala delle unità di visualizzazione come uno dei valori predefiniti in C#.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/axisdisplayunit/unit/
---
## AxisDisplayUnit.Unit property

Ottiene o imposta il valore di scala delle unità di visualizzazione come uno dei valori predefiniti.

```csharp
public AxisBuiltInUnit Unit { get; set; }
```

## Osservazioni

Il valore predefinito èNone . ILCustom e Percentage i valori non sono disponibili in alcuni tipi di grafico; vedi [`AxisBuiltInUnit`](../../axisbuiltinunit/) per ulteriori informazioni.

## Esempi

Mostra come manipolare i segni di graduazione e i valori visualizzati di un asse del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Imposta i segni di graduazione minori dell'asse Y in modo che puntino lontano dall'area del tracciato,
// e i principali segni di spunta per attraversare l'asse.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Imposta l'asse Y in modo che mostri un segno di spunta maggiore ogni 10 unità e un segno di spunta minore ogni 1 unità.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Imposta i limiti dell'asse Y su -10 e 20.
// Questo asse Y ora visualizzerà 4 segni di graduazione principali e 27 segni di graduazione minori.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Per l'asse X, imposta i segni di graduazione principali ogni 10 unità,
// ogni segno di spunta minore a 2,5 unità.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configura entrambi i tipi di segni di graduazione in modo che vengano visualizzati all'interno dell'area del tracciato del grafico.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Imposta i limiti dell'asse X in modo che l'asse X si estenda su 5 segni di graduazione principali e 12 segni di graduazione minori.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Imposta le etichette dei segni di spunta per visualizzarne il valore in milioni.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Possiamo impostare un valore più specifico in base al quale le etichette dei segni di spunta mostreranno i loro valori.
// Questa affermazione è equivalente a quella sopra.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Guarda anche

* enum [AxisBuiltInUnit](../../axisbuiltinunit/)
* class [AxisDisplayUnit](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
