---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: .NET için Aspose.Words
description: Grafik öğelerinizi etkili bir şekilde özelleştirmek için ChartFormat ShapeType özelliğini nasıl kullanacağınızı keşfedin. Veri görselleştirmenizi bugün geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Üst grafik öğesinin şekil türünü alır veya ayarlar.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## Notlar

Şu anda, özellik yalnızca veri etiketleri için kullanılabilir.

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

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
