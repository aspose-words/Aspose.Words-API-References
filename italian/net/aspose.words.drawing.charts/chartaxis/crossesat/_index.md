---
title: ChartAxis.CrossesAt
second_title: Aspose.Words per .NET API Reference
description: ChartAxis proprietà. Specifica il punto in cui lasse si incrocia sullasse perpendicolare.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Specifica il punto in cui l'asse si incrocia sull'asse perpendicolare.

```csharp
public double CrossesAt { get; set; }
```

### Osservazioni

La proprietà ha effetto solo se[`Crosses`](../crosses/) sono impostati suCustom. Non è supportato dai nuovi grafici di MS Office 2016.

Le unità sono determinate dal tipo di asse. Quando l'asse è un asse dei valori, il valore di property è un numero decimale sull'asse dei valori. Quando l'asse è un asse di categorie temporali, il valore è definito come un numero intero di giorni relativo alla data di base (30/12/1899). Per un asse di categorie di testo, il valore è un numero intero di categoria, iniziando con 1 come prima categoria.

### Esempi

Mostra come fare in modo che un asse del grafico si intersechi in una posizione personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Per i grafici a colonne, l'asse Y incrocia lo zero per impostazione predefinita,
// il che significa che le colonne per tutti i valori inferiori allo zero puntano verso il basso per rappresentare i valori negativi.
// Possiamo impostare un valore diverso per l'incrocio dell'asse Y. In questo caso lo imposteremo su 3.
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


