---
title: DocumentBuilder.InsertChart
linktitle: InsertChart
articleTitle: InsertChart
second_title: Aspose.Words para .NET
description: Mejore sus documentos fácilmente con el método InsertChart de DocumentBuilder. Agregue y redimensione gráficos fácilmente para lograr presentaciones impactantes.
type: docs
weight: 280
url: /es/net/aspose.words/documentbuilder/insertchart/
---
## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double*) {#insertchart_2}

Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| chartType | ChartType | El tipo de gráfico que se insertará en el documento. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar un gráfico circular en un documento.

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

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), double, double, [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_3}

Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertChart(ChartType chartType, double width, double height, ChartStyle chartStyle)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| chartType | ChartType | El tipo de gráfico que se insertará en el documento. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| chartStyle | ChartStyle | El estilo del gráfico insertado. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertchart}

Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| chartType | ChartType | El tipo de gráfico que se insertará en el documento. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo especificar la posición y el ajuste al insertar un gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertChart(ChartType.Pie, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
    100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertedChartRelativePosition.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertChart(*[ChartType](../../../aspose.words.drawing.charts/charttype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/), [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)*) {#insertchart_1}

Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertChart(ChartType chartType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType, 
    ChartStyle chartStyle)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| chartType | ChartType | El tipo de gráfico que se insertará en el documento. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |
| chartStyle | ChartStyle | El estilo del gráfico insertado. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
