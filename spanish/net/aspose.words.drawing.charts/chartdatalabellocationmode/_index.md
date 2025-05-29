---
title: ChartDataLabelLocationMode Enum
linktitle: ChartDataLabelLocationMode
articleTitle: ChartDataLabelLocationMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.ChartDataLabelLocationMode para personalizar de manera efectiva la posición de la etiqueta de datos con configuraciones de propiedades intuitivas Izquierda y Superior.
type: docs
weight: 950
url: /es/net/aspose.words.drawing.charts/chartdatalabellocationmode/
---
## ChartDataLabelLocationMode enumeration

Especifica cómo se representan los valores que especifican la ubicación de una etiqueta de datos:[`Left`](../chartdatalabel/left/) y [`Top`](../chartdatalabel/top/) propiedades - se interpretan.

```csharp
public enum ChartDataLabelLocationMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Offset | `0` | La ubicación de una etiqueta de datos se especifica mediante un desplazamiento desde la posición definida por its [`Position`](../chartdatalabel/position/) propiedad. |
| Absolute | `1` | La ubicación de una etiqueta de datos se especifica utilizando coordenadas absolutas, comenzando desde la esquina superior izquierda de un gráfico. |

## Ejemplos

Muestra cómo colocar las etiquetas de datos del gráfico de anillos fuera del anillo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
//Eliminar serie generada por defecto.
seriesColl.Clear();

// Ocultar la leyenda.
chart.Legend.Position = LegendPosition.None;

//Generar datos.
const int dataLength = 20;
double totalValue = 0;
string[] categories = new string[dataLength];
double[] values = new double[dataLength];

for (int i = 0; i < dataLength; i++)
{
    categories[i] = $"Category {i}";
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

ChartSeries series = seriesColl.Add("Series 1", categories, values);
series.HasDataLabels = true;

ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.ShowLeaderLines = true;

La propiedad Posición no se puede usar para gráficos de anillos. Coloquemos las etiquetas de datos usando las opciones Izquierda y Superior.
// propiedades alrededor de un círculo fuera del gráfico de anillos.
//El origen está en la esquina superior izquierda del gráfico.

const double titleAreaHeight = 25.5; // Esto se puede calcular utilizando el texto del título y la fuente.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Esto se puede calcular utilizando la fuente de la etiqueta.
const double oneCharLabelWidth = 12.75; // Esto se puede calcular para cada etiqueta usando su texto y fuente.
const double twoCharLabelWidth = 17.25; // Esto se puede calcular para cada etiqueta usando su texto y fuente.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Debido a que los puntos de datos comienzan en la parte superior, las coordenadas X utilizadas en las propiedades Izquierda y Superior de
// Las etiquetas de datos apuntan hacia la derecha y las coordenadas Y apuntan hacia abajo, el ángulo inicial es -PI/2.
double totalAngle = -System.Math.PI / 2;
ChartDataLabel previousLabel = null;

for (int i = 0; i < series.YValues.Count; i++)
{
    ChartDataLabel dataLabel = dataLabels[i];

    double value = series.YValues[i].DoubleValue;
    double labelWidth;
    if (value < 10)
        labelWidth = oneCharLabelWidth;
    else
        labelWidth = twoCharLabelWidth;
    double labelSegmentAngle = value / totalValue * 2 * System.Math.PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System.Math.Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System.Math.Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // Si la etiqueta de datos actual se superpone a otras etiquetas, muévala horizontalmente.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Muévete hacia la derecha en la parte superior y hacia la izquierda en la parte inferior.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System.Math.PI);
        int factor;
        if (isOnTop)
            factor = 1;
        else
            factor = -1;

        labelLeft = previousLabel.Left + labelWidth * factor + labelMargin;
    }

    dataLabel.Left = labelLeft;
    dataLabel.LeftMode = ChartDataLabelLocationMode.Absolute;
    dataLabel.Top = labelTop;
    dataLabel.TopMode = ChartDataLabelLocationMode.Absolute;

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc.Save(ArtifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
