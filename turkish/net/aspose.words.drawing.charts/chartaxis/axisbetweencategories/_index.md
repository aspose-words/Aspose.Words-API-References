---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words for .NET
description: ChartAxis AxisBetweenCategories mülk. Değer ekseninin kategoriler arasında kategori eksenini geçip geçmediğini gösteren bir bayrak alır veya ayarlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Değer ekseninin kategoriler arasında kategori eksenini geçip geçmediğini gösteren bir bayrak alır veya ayarlar.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Notlar

Özelliğin yalnızca değer eksenleri için etkisi vardır. MS Office 2016 yeni çizelgeleri tarafından desteklenmemektedir.

## Örnekler

Özel bir konumda kesişecek bir grafik ekseninin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Sütun grafikleri için Y ekseni varsayılan olarak sıfırdan geçer,
// bu, sıfırın altındaki tüm değerlerin sütunlarının negatif değerleri temsil edecek şekilde aşağıyı gösterdiği anlamına gelir.
// Y ekseni geçişi için farklı bir değer ayarlayabiliriz. Bu durumda 3'e ayarlayacağız.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Ayrıca bakınız

* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
