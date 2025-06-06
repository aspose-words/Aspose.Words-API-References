---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.AxisBound, su solución para definir límites de valores de ejes en gráficos para una visualización de datos precisa.
type: docs
weight: 750
url: /es/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Representa el límite mínimo o máximo de los valores del eje.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public sealed class AxisBound
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Crea una nueva instancia que indica que el límite del eje debe ser determinado automáticamente por una aplicación de procesamiento de textos. |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | Crea un límite de eje representado como un valor de fecha y hora. |
| [AxisBound](axisbound/#constructor_1)(*double*) | Crea un límite de eje representado como un número. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Devuelve un indicador que indica que el límite del eje debe determinarse automáticamente. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Devuelve el valor numérico del límite del eje. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Devuelve el valor del límite del eje representado como fecha y hora. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Sirve como una función hash para este tipo. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Devuelve una cadena fácil de usar que muestra el valor de este objeto. |

## Observaciones

El límite se puede especificar como un valor numérico, de fecha y hora o un valor "automático" especial.

Las instancias de esta clase son inmutables.

## Ejemplos

Muestra cómo insertar un gráfico con valores de fecha y hora.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada que contenga valores de fecha y hora para el eje X y valores decimales respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Establezca límites inferior y superior para el eje X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Establezca las unidades principales del eje X en una semana y las unidades secundarias en un día.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Define las propiedades del eje Y para valores decimales.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
