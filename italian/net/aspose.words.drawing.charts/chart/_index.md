---
title: Class Chart
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.Chart classe. Fornisce laccesso alle proprietà della forma del grafico.
type: docs
weight: 600
url: /it/net/aspose.words.drawing.charts/chart/
---
## Chart class

Fornisce l'accesso alle proprietà della forma del grafico.

```csharp
public class Chart
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Fornisce l'accesso alle proprietà dell'asse X del grafico. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Fornisce l'accesso alle proprietà dell'asse Y del grafico. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Fornisce l'accesso alle proprietà dell'asse Z del grafico. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Fornisce l'accesso alle proprietà della legenda del grafico. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Fornisce l'accesso alla raccolta di serie. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Ottiene il percorso e il nome di un file xls/xlsx a cui questo grafico è collegato. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Fornisce l'accesso alle proprietà del titolo del grafico. |

### Esempi

Mostra come inserire un grafico e impostare un titolo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma di grafico con un generatore di documenti e ottieni il suo grafico.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Usa la proprietà "Titolo" per assegnare un titolo al nostro grafico, che appare in alto al centro dell'area del grafico.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Imposta la proprietà "Mostra" su "true" per rendere visibile il titolo.
title.Show = true;

// Imposta la proprietà "Overlay" su "true" Assegna più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


