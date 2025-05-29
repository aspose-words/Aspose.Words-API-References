---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: .NET için Aspose.Words
description: Veri etiketleriniz için özelleştirilebilir dolgu ve çizgi biçimlendirmesine kolay erişim için ChartDataLabelCollection Format özelliğini keşfedin. Grafiklerinizi bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Veri etiketlerinin dolgu ve satır biçimlendirmesine erişim sağlar.

```csharp
public ChartFormat Format { get; }
```

## Örnekler

Grafik veri etiketleri için dolgu, kontur ve açıklama biçimlendirmesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Yeni seri ekle.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Veri etiketlerini göster.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Veri etiketlerini açıklama metinleri olarak biçimlendir.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Bireysel veri etiketinin dolgusunu ve çizgisini değiştir.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Ayrıca bakınız

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
