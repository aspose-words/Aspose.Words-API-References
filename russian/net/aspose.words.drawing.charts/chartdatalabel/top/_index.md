---
title: ChartDataLabel.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words для .NET
description: Настройте свойство ChartDataLabel Top, чтобы управлять позиционированием меток данных для повышения ясности диаграммы. Оптимизируйте визуальное представление данных без усилий!
type: docs
weight: 210
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/top/
---
## ChartDataLabel.Top property

Возвращает или задает расстояние метки данных в пунктах от верхнего края диаграммы или от позиции , указанной ее[`Position`](../position/) имущества, в зависимости от стоимости[`TopMode`](../topmode/) свойство.

```csharp
public double Top { get; set; }
```

## Примечания

Значение свойства изменяется пропорционально при изменении размера диаграммы.

Свойство невозможно задать в диаграмме Word 2016.

## Примеры

Показывает, как размещать метки данных кольцевой диаграммы за пределами кольцевой диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Удалить сгенерированную по умолчанию серию.
seriesColl.Clear();

// Скрыть легенду.
chart.Legend.Position = LegendPosition.None;

// Генерация данных.
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

// Свойство Position не может использоваться для кольцевых диаграмм. Давайте разместим метки данных с помощью Left и Top
// свойства по окружности за пределами диаграммы-пончика.
// Начало координат находится в верхнем левом углу графика.

const double titleAreaHeight = 25.5; // Это можно рассчитать, используя текст заголовка и шрифт.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Это можно рассчитать с помощью шрифта метки.
const double oneCharLabelWidth = 12.75; // Это можно рассчитать для каждой метки, используя ее текст и шрифт.
const double twoCharLabelWidth = 17.25; // Это можно рассчитать для каждой метки, используя ее текст и шрифт.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Поскольку точки данных начинаются сверху, координаты X, используемые в свойствах Left и Top
// метки данных указывают вправо, а координаты Y указывают вниз, начальный угол равен -PI/2.
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

    // Если текущая метка данных перекрывает другие метки, переместите ее по горизонтали.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Двигаемся вправо вверху, влево вниз.
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

### Смотрите также

* class [ChartDataLabel](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
