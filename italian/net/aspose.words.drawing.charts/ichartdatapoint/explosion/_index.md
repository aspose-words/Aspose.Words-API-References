---
title: IChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words per .NET
description: Scopri la proprietà IChartDataPoint Explosion per i grafici a torta. Controlla il posizionamento dei punti dati con precisione: migliora la narrazione visiva dei tuoi dati oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Specifica di quanto deve essere spostato il punto dati dal centro della torta. Può essere negativo, negativo significa che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta.

```csharp
public int Explosion { get; set; }
```

## Esempi

Mostra come spostare le fette di un grafico a torta lontano dal centro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Le "fette" di un grafico a torta possono essere spostate lontano dal centro tramite l'attributo Esplosione del rispettivo punto dati.
// Aggiungere un punto dati alla prima porzione del grafico a torta e spostarlo di 10 punti dal centro.
// Aspose.Words crea automaticamente punti dati se questi non esistono.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Sposta la seconda porzione di una distanza maggiore.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Guarda anche

* interface [IChartDataPoint](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
