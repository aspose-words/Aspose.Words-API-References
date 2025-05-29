---
title: AxisScaling.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà Tipo AxisScaling per personalizzare facilmente il ridimensionamento degli assi. Migliora la visualizzazione dei dati con impostazioni flessibili per una chiarezza ottimale.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

Ottiene o imposta il tipo di ridimensionamento dell'asse.

```csharp
public AxisScaleType Type { get; set; }
```

## Osservazioni

IlLinearil valore è l'unico consentito nei nuovi grafici di MS Office 2016.

## Esempi

Mostra come applicare la scala logaritmica a un asse di un grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Inserisci una serie con coordinate X/Y per cinque punti.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Per impostazione predefinita, la scala dell'asse X è lineare,
// visualizza valori con incremento uniforme che coprono l'intervallo del valore X (0, 1, 2, 3...).
// Un asse lineare non è l'ideale per i nostri valori Y
// poiché i punti con valori Y più piccoli saranno più difficili da leggere.
// Una scala logaritmica con base 20 (1, 20, 400, 8000...)
// distribuirà i punti tracciati, consentendoci di leggere più facilmente i loro valori sul grafico.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Guarda anche

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
