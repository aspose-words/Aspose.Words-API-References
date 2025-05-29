---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ShowBubbleSize migliora i tuoi grafici a bolle visualizzando le dimensioni delle etichette dati. Ottimizza la rappresentazione visiva dei tuoi dati oggi stesso!
type: docs
weight: 130
url: /it/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati su un grafico. Si applica solo ai grafici a bolle. Il valore predefinito è `falso` .

```csharp
public bool ShowBubbleSize { get; set; }
```

## Esempi

Mostra come utilizzare gli effetti 3D con i grafici a bolle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Applica un'etichetta dati a ciascuna bolla che ne visualizza il diametro.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Guarda anche

* class [ChartDataLabel](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
