---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: .NET için Aspose.Words
description: Grafiklerinizdeki etiket açılarını kolayca özelleştirmek için ChartDataLabel Rotation özelliğini keşfedin. Hassas kontrolle veri görselleştirmeyi geliştirin!
type: docs
weight: 110
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

Etiketin dönüşünü derece cinsinden alır veya ayarlar.

```csharp
public int Rotation { get; set; }
```

## Notlar

Kabul edilebilir değerler aralığı -180 ile 180 dahil arasındadır. Varsayılan değer 0'dır.

Eğer[`Orientation`](../orientation/) değerHorizontal varsa etiket şekli, etiket metniyle birlikte döndürülür. Aksi takdirde, yalnızca etiket metni döndürülür.

## Örnekler

Veri etiketleri için yönelim ve dönüşün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Veri etiketlerini göster.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Veri etiketi şeklini tanımlayın.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Tüm seri için veri etiketi yönünü ve dönüşünü ayarlayın.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// İlk veri etiketinin yönünü ve dönüşünü değiştir.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Ayrıca bakınız

* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
