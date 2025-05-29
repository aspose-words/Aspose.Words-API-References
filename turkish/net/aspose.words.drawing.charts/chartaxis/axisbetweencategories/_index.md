---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: .NET için Aspose.Words
description: ChartAxis AxisBetweenCategories özelliğini keşfedin—grafiklerinizde gelişmiş kategori görselleştirmesi için değer ekseni konumlandırmasını kontrol edin. Veri sunumunuzu optimize edin!
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Kategoriler arasında değer ekseninin kategori eksenini geçip geçmediğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Notlar

Özellik yalnızca değer eksenleri için etkilidir. MS Office 2016 yeni grafikleri tarafından desteklenmez.

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
