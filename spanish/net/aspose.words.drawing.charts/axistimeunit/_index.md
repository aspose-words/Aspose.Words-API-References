---
title: AxisTimeUnit Enum
linktitle: AxisTimeUnit
articleTitle: AxisTimeUnit
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.Charts.AxisTimeUnit su solución para definir unidades de tiempo en los ejes del gráfico de manera eficiente y eficaz.
type: docs
weight: 860
url: /es/net/aspose.words.drawing.charts/axistimeunit/
---
## AxisTimeUnit enumeration

Especifica la unidad de tiempo para los ejes.

```csharp
public enum AxisTimeUnit
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Automatic | `0` | Especifica que la unidad no se configuró explícitamente y se debe utilizar el valor predeterminado. |
| Days | `1` | Especifica que los datos del gráfico se mostrarán en días. |
| Months | `2` | Especifica que los datos del gráfico se mostrarán en meses. |
| Years | `3` | Especifica que los datos del gráfico se mostrarán en años. |

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
