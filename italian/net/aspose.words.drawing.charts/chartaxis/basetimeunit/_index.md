---
title: ChartAxis.BaseTimeUnit
linktitle: BaseTimeUnit
articleTitle: BaseTimeUnit
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxis BaseTimeUnit per definire facilmente l'unità di tempo più piccola sull'asse delle categorie temporali per una migliore visualizzazione dei dati.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartaxis/basetimeunit/
---
## ChartAxis.BaseTimeUnit property

Restituisce o imposta l'unità di tempo più piccola rappresentata sull'asse della categoria temporale.

```csharp
public AxisTimeUnit BaseTimeUnit { get; set; }
```

## Osservazioni

La proprietà ha effetto solo per gli assi della categoria temporale.

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

* enum [AxisTimeUnit](../../axistimeunit/)
* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
