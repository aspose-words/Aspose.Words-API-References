---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirme ve netlik için veri etiketi konumlarınızı kolayca özelleştirmek üzere ChartDataLabelCollection Position özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

Veri etiketlerinin konumunu alır veya ayarlar.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Notlar

Aşağıdaki grafik serisi türlerinin veri etiketleri için konum ayarlanabilir:

-Bar ,Column , Histogram ,Pareto , Waterfall ; izin verilen değerler:Center , InsideBase ,InsideEnd ve OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; allowed değerleri:Center ,InsideBase veInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock ; izin verilen değerler:Center , Left ,Right , Above VeBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie ; izin verilen değerler: Center ,InsideEnd , OutsideEnd VeBestFit;

-BoxAndWhisker ; izin verilen değerler: Left ,Right , Above VeBelow.

## Örnekler

Veri etiketinin konumunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sütun grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Varsayılan olarak oluşturulan seriyi sil.
seriesColl.Clear();

// Seri ekle.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Veri etiketlerini göster ve yazı tipi rengini ayarla.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Veri etiketi konumunu ayarla.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Ayrıca bakınız

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
