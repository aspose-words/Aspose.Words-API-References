---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti senza sforzo con il metodo InsertChart di DocumentBuilder. Aggiungi e ridimensiona facilmente gli oggetti grafico per presentazioni di grande impatto.
type: docs
weight: 280
url: /it/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_2}

Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | ChartType | Tipo di grafico da inserire nel documento. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un grafico a torta in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, ConvertUtil.PixelToPoint(300), 
    ConvertUtil.PixelToPoint(300)).Chart;
chart.Series.Clear();
chart.Series.Add("My fruit",
    new[] { "Apples", "Bananas", "Cherries" },
    new[] { 1.3, 2.2, 1.5 });

doc.Save(ArtifactsDir + "DocumentBuilder.InsertPieChart.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_3}

Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height, ChartStyle chartStyle)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | ChartType | Tipo di grafico da inserire nel documento. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| chartStyle | ChartStyle | Lo stile del grafico inserito. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | ChartType | Tipo di grafico da inserire nel documento. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine alla parte superiore dell'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come disporre il testo attorno all'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/), [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_1}

Inserisce un oggetto grafico nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType, 
    ChartStyle chartStyle)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | ChartType | Tipo di grafico da inserire nel documento. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine alla parte superiore dell'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come disporre il testo attorno all'immagine. |
| chartStyle | ChartStyle | Lo stile del grafico inserito. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
