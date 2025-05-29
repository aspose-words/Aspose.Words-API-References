---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: Personalizza le impostazioni del font di ChartLegend senza sforzo! Accedi alla formattazione predefinita e sostituisci facilmente voci specifiche della legenda per un look impeccabile.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Fornisce l'accesso alla formattazione predefinita del carattere per le voci della legenda. Per sovrascrivere la formattazione del carattere per una specifica voce della legenda, utilizzare[`Font`](../../chartlegendentry/font/) proprietà.

```csharp
public Font Font { get; }
```

## Esempi

Mostra come lavorare con un font di legenda.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Imposta la dimensione predefinita del carattere per tutte le voci della legenda.
chartLegend.Font.Size = 14;
// Cambia il font per una voce specifica della legenda.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Ottieni la voce della legenda per la serie di grafici.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Guarda anche

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
