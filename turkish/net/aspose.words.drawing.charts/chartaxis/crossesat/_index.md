---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için grafiğinizin dik eksenindeki kesişim noktalarını kolayca tanımlamak üzere ChartAxis CrossesAt özelliğini keşfedin.
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

Mülkiyet ancak aşağıdaki durumlarda geçerlidir:[`Crosses`](../crosses/) ayarlandıCustom. MS Office 2016 yeni grafikleri tarafından desteklenmiyor.

Birimler eksen türüne göre belirlenir. Eksen bir değer ekseni olduğunda, property değeri değer ekseninde bir ondalık sayıdır. Eksen bir zaman kategorisi ekseni olduğunda, değer temel tarihe (30/12/1899) göre tam sayı gün sayısı olarak tanımlanır. Metin kategorisi ekseni için değer, ilk kategori olarak 1 ile başlayan tam sayı kategori numarasıdır.

## Örnekler

Bir grafik ekseninin özel bir konumda nasıl kesişeceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Sütun grafikleri için Y ekseni varsayılan olarak sıfırı geçer,
// bu, sıfırın altındaki tüm değerler için sütunların negatif değerleri temsil edecek şekilde aşağıya doğru işaret ettiği anlamına gelir.
// Y ekseni geçişi için farklı bir değer ayarlayabiliriz. Bu durumda, bunu 3 olarak ayarlayacağız.
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
