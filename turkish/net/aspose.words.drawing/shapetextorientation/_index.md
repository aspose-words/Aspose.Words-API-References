---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: .NET için Aspose.Words
description: Şekillerdeki metin yönünü kolayca kontrol etmek, belge tasarımınızı ve okunabilirliğinizi geliştirmek için Aspose.Words.Drawing.ShapeTextOrientation enum'unu keşfedin.
type: docs
weight: 1680
url: /tr/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Şekillerdeki metnin yönünü belirtir.

```csharp
public enum ShapeTextOrientation
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Horizontal | `0` | Metin yatay olarak düzenlenmiştir (lr-tb). |
| Downward | `1` | Metin yukarıdan aşağıya doğru görünecek şekilde 90 derece sağa döndürülür (tb-rl). |
| Upward | `2` | Metin, aşağıdan yukarıya doğru görünecek şekilde 90 derece sola döndürülür (bt-lr). |
| VerticalFarEast | `3` | Uzak Doğu karakterleri dikey görünür, diğer metin yukarıdan aşağıya doğru görünmesi için 90 derece sağa döndürülür (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Uzak Doğu karakterleri dikey görünür, diğer metinler 90 derece sağa döndürülür ve dikey olarak yukarıdan aşağıya, sonra yatay olarak soldan sağa (tb-lr-v) görünür. |
| WordArtVertical | `5` | Metin dikeydir ve bir harf diğerinin üstündedir. |
| WordArtVerticalRightToLeft | `6` | Metin dikeydir, bir harf diğerinin üstündedir, sonra yatay olarak sağdan sola. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
