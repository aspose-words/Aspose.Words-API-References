---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.ChartLegendEntry per creare legende dinamiche per grafici. Migliora la visualizzazione dei tuoi dati con un'integrazione e una personalizzazione perfette.
type: docs
weight: 1020
url: /it/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Rappresenta una voce della legenda del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartLegendEntry
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questa voce della legenda. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Ottiene o imposta un valore che indica se questa voce è nascosta nella legenda del grafico. Il valore predefinito è**falso** . |

## Osservazioni

Una voce della legenda corrisponde a una serie di grafici o a una linea di tendenza specifica.

Il testo della voce è il nome della serie o della linea di tendenza. Il testo non può essere modificato.

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
