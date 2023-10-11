---
title: AxisBound.Value
second_title: Referencia de API de Aspose.Words para .NET
description: AxisBound propiedad. Devuelve el valor numérico del límite del eje.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/axisbound/value/
---
## AxisBound.Value property

Devuelve el valor numérico del límite del eje.

```csharp
public double Value { get; }
```

### Ejemplos

Muestra cómo establecer límites de eje personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Borra la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agrega una serie con dos matrices decimales. La primera matriz contiene los valores X,
// y el segundo contiene los valores Y correspondientes a los puntos del gráfico de dispersión.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// De forma predeterminada, la escala predeterminada se aplica a los ejes X e Y del gráfico,
// para que ambos rangos sean lo suficientemente grandes como para abarcar todos los valores X e Y de cada serie.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Podemos definir nuestros propios límites de eje.
// En este caso, haremos que las reglas de los ejes X e Y muestren un rango de 0 a 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Cree un gráfico de líneas con una serie que requiera un rango de fechas en el eje X y valores decimales para el eje Y.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// También podemos establecer límites de ejes en forma de fechas, limitando el gráfico a un período.
// Establecer el rango en 1980-1990 omitirá los dos valores de la serie
// que están fuera del rango del gráfico.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Ver también

* class [AxisBound](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../axisbound/)
* asamblea [Aspose.Words](../../../)


