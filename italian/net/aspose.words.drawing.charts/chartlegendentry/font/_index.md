---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font di ChartLegendEntry per accedere facilmente alla formattazione dei font personalizzabile, migliorando le voci della legenda e rendendole più accattivanti dal punto di vista visivo.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Fornisce l'accesso alla formattazione del carattere di questa voce della legenda.

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
* class [ChartLegendEntry](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
