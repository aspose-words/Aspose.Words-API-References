---
title: AxisBound.AxisBound
second_title: Referencia de API de Aspose.Words para .NET
description: AxisBound constructor. Crea una nueva instancia que indica que el límite del eje debe determinarse automáticamente mediante una aplicación de procesamiento de texto.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound() {#constructor}

Crea una nueva instancia que indica que el límite del eje debe determinarse automáticamente mediante una aplicación de procesamiento de texto.

```csharp
public AxisBound()
```

### Ejemplos

Muestra cómo establecer límites de eje personalizados.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agrega una serie con dos arreglos decimales. La primera matriz contiene los valores de X,
// y el segundo contiene valores Y correspondientes para puntos en el gráfico de dispersión.
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

// También podemos establecer límites de eje en forma de fechas, limitando el gráfico a un período.
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

---

## AxisBound(double) {#constructor_1}

Crea un límite de eje representado como un número.

```csharp
public AxisBound(double value)
```

### Ejemplos

Muestra cómo insertar un gráfico con valores de fecha/hora.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada que contenga valores de fecha/hora para el eje X y valores decimales respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Establecer límites inferior y superior para el eje X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Establecer las unidades principales del eje X en una semana y las unidades secundarias en un día.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Definir propiedades del eje Y para valores decimales.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ver también

* class [AxisBound](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../axisbound/)
* asamblea [Aspose.Words](../../../)

---

## AxisBound(DateTime) {#constructor_2}

Crea un límite de eje representado como valor de fecha y hora.

```csharp
public AxisBound(DateTime datetime)
```

### Ejemplos

Muestra cómo insertar un gráfico con valores de fecha/hora.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada que contenga valores de fecha/hora para el eje X y valores decimales respectivos para el eje Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Establecer límites inferior y superior para el eje X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Establecer las unidades principales del eje X en una semana y las unidades secundarias en un día.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Definir propiedades del eje Y para valores decimales.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ver también

* class [AxisBound](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../axisbound/)
* asamblea [Aspose.Words](../../../)


