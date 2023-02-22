---
title: ChartAxis.CrossesAt
second_title: Aspose.Words per .NET API Reference
description: ChartAxis proprietà. Specifica dove si incrocia lasse sullasse perpendicolare.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Specifica dove si incrocia l'asse sull'asse perpendicolare.

```csharp
public double CrossesAt { get; set; }
```

### Osservazioni

La proprietà ha effetto solo se[`Crosses`](../crosses/) sono impostati suCustom. Non è supportato dai nuovi grafici di MS Office 2016.

Le unità sono determinate dal tipo di asse. Quando l'asse è un asse del valore, il valore della proprietà è un numero decimale sull'asse del valore. Quando l'asse è un asse di categoria temporale, il valore è definito come un numero intero di giorni relativo alla data base (30/12/1899). Per un asse di categoria di testo, il valore è un numero di categoria intero, che inizia con 1 come prima categoria.

### Esempi

Mostra come far incrociare un asse del grafico in una posizione personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Per gli istogrammi, l'asse Y incrocia lo zero per impostazione predefinita,
// il che significa che le colonne per tutti i valori inferiori allo zero puntano verso il basso per rappresentare valori negativi.
// Possiamo impostare un valore diverso per l'incrocio dell'asse Y. In questo caso, lo imposteremo a 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Guarda anche

* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartaxis/)
* assemblea [Aspose.Words](../../../)


