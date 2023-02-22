---
title: DocumentBuilder.InsertChart
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.
type: docs
weight: 260
url: /it/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(ChartType, double, double) {#insertchart_1}

Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | ChartType | Il tipo di grafico da inserire nel documento. |
| width | Double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo dell'immagine che è stato appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

### Esempi

Mostra come inserire un grafico a torta in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, ConvertUtil.PixelToPoint(300), 
    ConvertUtil.PixelToPoint(300)).Chart;
chart.Series.Add("My fruit",
    new[] { "Apples", "Bananas", "Cherries" },
    new[] { 1.3, 2.2, 1.5 });

doc.Save(ArtifactsDir + "DocumentBuilder.InsertPieChart.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertChart(ChartType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertchart}

Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | ChartType | Il tipo di grafico da inserire nel documento. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine al lato superiore dell'immagine. |
| width | Double | La larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | L'altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come avvolgere il testo attorno all'immagine. |

### Valore di ritorno

Il nodo dell'immagine che è stato appena inserito.

### Osservazioni

È possibile modificare la dimensione dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

### Esempi

Mostra come specificare la posizione e l'avvolgimento durante l'inserimento di un grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


