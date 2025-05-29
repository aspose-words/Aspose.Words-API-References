---
title: ChartAxis.MinorUnitIsAuto
linktitle: MinorUnitIsAuto
articleTitle: MinorUnitIsAuto
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ChartAxis MinorUnitIsAuto ottimizza le tacche dei tuoi grafici per una visualizzazione dei dati più chiara. Migliora i tuoi grafici senza sforzo!
type: docs
weight: 180
url: /it/net/aspose.words.drawing.charts/chartaxis/minorunitisauto/
---
## ChartAxis.MinorUnitIsAuto property

Ottiene o imposta un flag che indica se deve essere utilizzata la distanza predefinita tra i segni di graduazione minori.

```csharp
public bool MinorUnitIsAuto { get; set; }
```

## Osservazioni

La proprietà ha effetto sugli assi della categoria temporale e dei valori.

## Esempi

Mostra come manipolare i segni di spunta e i valori visualizzati di un asse del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Imposta i segni di spunta minori dell'asse Y in modo che puntino lontano dall'area del grafico,
// e i segni di spunta principali per attraversare l'asse.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Imposta l'asse Y in modo da mostrare un tick principale ogni 10 unità e un tick secondario ogni 1 unità.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Imposta i limiti dell'asse Y su -10 e 20.
// Questo asse Y ora visualizzerà 4 tacche principali e 27 tacche secondarie.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Per l'asse X, imposta i segni di spunta principali ogni 10 unità,
// ogni piccolo segno di spunta a 2,5 unità.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configura entrambi i tipi di segni di spunta in modo che appaiano all'interno dell'area del grafico.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Imposta i limiti dell'asse X in modo che l'asse X copra 5 tacche principali e 12 tacche secondarie.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Imposta le etichette dei tick per visualizzare il loro valore in milioni.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Possiamo impostare un valore più specifico in base al quale le etichette delle tacche visualizzeranno i loro valori.
// Questa affermazione è equivalente a quella precedente.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Guarda anche

* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
