---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words for .NET
description: ChartAxis CrossesAt mülk. Eksenin dik eksende nerede kesiştiğini belirtir C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Eksenin dik eksende nerede kesiştiğini belirtir.

```csharp
public double CrossesAt { get; set; }
```

## Notlar

Özelliğin yalnızca şu durumlarda etkisi vardır:[`Crosses`](../crosses/) şu şekilde ayarlandı:Custom. MS Office 2016 yeni çizelgeleri tarafından desteklenmemektedir.

Birimler eksen türüne göre belirlenir. Eksen bir değer ekseni olduğunda, property özelliğinin değeri, değer ekseninde bir ondalık sayıdır. Eksen bir zaman kategorisi ekseni olduğunda değer, temel tarihe (30/12/1899) göre günlerin tam sayısı olan olarak tanımlanır. Bir metin kategorisi ekseni için değer, ilk kategori olarak 1 ile başlayan bir tamsayı kategori numarasıdır .

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
