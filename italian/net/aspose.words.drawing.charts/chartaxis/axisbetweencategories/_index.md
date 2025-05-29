---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxis AxisBetweenCategories: controlla il posizionamento dell'asse dei valori per una migliore visualizzazione delle categorie nei tuoi grafici. Ottimizza la presentazione dei tuoi dati!
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Ottiene o imposta un flag che indica se l'asse dei valori attraversa l'asse delle categorie tra le categorie.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Osservazioni

La proprietà ha effetto solo sugli assi dei valori. Non è supportata dai nuovi grafici di MS Office 2016.

## Esempi

Mostra come far sì che un asse del grafico si intersechi in una posizione personalizzata.

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
// che significa che le colonne per tutti i valori inferiori a zero puntano verso il basso per rappresentare i valori negativi.
// Possiamo impostare un valore diverso per l'incrocio dell'asse Y. In questo caso, lo imposteremo a 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Guarda anche

* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
