---
title: ChartAxis.CrossesAt
second_title: Aspose.Words for .NET API Referansı
description: ChartAxis mülk. Eksenin dikey eksende kesiştiği yeri belirtir.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Eksenin dikey eksende kesiştiği yeri belirtir.

```csharp
public double CrossesAt { get; set; }
```

### Notlar

Mülkiyet ancak şu durumlarda etkilidir:[`Crosses`](../crosses/) ayarlandıCustom. MS Office 2016 yeni çizelgeleri tarafından desteklenmez.

Birimler eksen tipine göre belirlenir. Eksen bir değer ekseni olduğunda, property öğesinin değeri, değer eksenindeki ondalık bir sayıdır. Eksen bir zaman kategorisi ekseni olduğunda, değer, temel tarihe (30/12/1899) göre bir tamsayı gün sayısı olarak tanımlanır. Bir metin kategorisi ekseni için, ilk kategori olarak 1 ile başlayan bir tamsayı kategori numarası değeridir.

### Örnekler

Özel bir konumda çaprazlanacak bir grafik ekseninin nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Sütun grafikler için, Y ekseni varsayılan olarak sıfırda kesişir,
// bu, sıfırın altındaki tüm değerler için sütunların negatif değerleri temsil etmesi anlamına gelir.
// Y ekseni geçişi için farklı bir değer ayarlayabiliriz. Bu durumda, 3'e ayarlayacağız.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Ayrıca bakınız

* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartaxis/)
* toplantı [Aspose.Words](../../../)


