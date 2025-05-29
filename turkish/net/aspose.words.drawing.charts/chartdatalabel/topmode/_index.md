---
title: ChartDataLabel.TopMode
linktitle: TopMode
articleTitle: TopMode
second_title: .NET için Aspose.Words
description: Grafiklerinizdeki veri etiketi konumlandırmasını özelleştirmek için ChartDataLabel TopMode özelliğini keşfedin. Görsel veri sunumlarınızda netliği ve hassasiyeti artırın!
type: docs
weight: 220
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/topmode/
---
## ChartDataLabel.TopMode property

Yorumlama modunu alır veya ayarlar[`Top`](../top/) özellik değeri: veri etiketinin location değerini grafiğin üst kenarından belirtilen konumdan ayarlayıp ayarlamadığı[`Position`](../position/) özelliği.

```csharp
public ChartDataLabelLocationMode TopMode { get; set; }
```

## Notlar

Özellik Word 2016 grafiğinde ayarlanamaz.

## Örnekler

Halka grafiğinin veri etiketlerinin halkanın dışına nasıl yerleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Varsayılan olarak oluşturulan seriyi sil.
seriesColl.Clear();

// Efsaneyi gizle.
chart.Legend.Position = LegendPosition.None;

// Veri üret.
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

// Position özelliği halka grafikler için kullanılamaz. Veri etiketlerini Sol ve Üst kullanarak yerleştirelim
// grafik halkasının dışındaki bir dairenin etrafındaki özellikler.
// Orijin, grafiğin sol üst köşesindedir.

const double titleAreaHeight = 25.5; // Bu, başlık metni ve yazı tipi kullanılarak hesaplanabilir.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // Bu, etiket yazı tipini kullanarak hesaplanabilir.
const double oneCharLabelWidth = 12.75; // Bu, her etiket için metni ve yazı tipini kullanarak hesaplanabilir.
const double twoCharLabelWidth = 17.25; // Bu, her etiket için metni ve yazı tipini kullanarak hesaplanabilir.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Veri noktaları üstten başladığından, Sol ve Üst özelliklerinde kullanılan X koordinatları
// veri etiketleri sağa, Y koordinatları aşağıya işaret ediyor, başlangıç açısı -PI/2'dir.
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

    // Mevcut veri etiketi diğer etiketlerle çakışıyorsa, yatay olarak taşıyın.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Üstte sağa, altta sola hareket et.
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

### Ayrıca bakınız

* enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
