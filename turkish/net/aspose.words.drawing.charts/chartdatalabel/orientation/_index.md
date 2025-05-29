---
title: ChartDataLabel.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: .NET için Aspose.Words
description: Grafiklerinizdeki veri görselleştirmesini ve netliği artırmak için etiket metni yönünü kolayca özelleştirmek amacıyla ChartDataLabel Yönlendirme özelliğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/orientation/
---
## ChartDataLabel.Orientation property

Etiket metninin yönünü alır veya ayarlar.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Notlar

Varsayılan değer:Horizontal .

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
