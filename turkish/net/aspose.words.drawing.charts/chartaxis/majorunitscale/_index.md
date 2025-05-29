---
title: ChartAxis.MajorUnitScale
linktitle: MajorUnitScale
articleTitle: MajorUnitScale
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için zaman kategorisi ekseninizdeki önemli onay işaretlerini kolayca özelleştirmek amacıyla ChartAxis MajorUnitScale özelliğini keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words.drawing.charts/chartaxis/majorunitscale/
---
## ChartAxis.MajorUnitScale property

Zaman kategorisi eksenindeki ana işaretler için ölçek değerini döndürür veya ayarlar.

```csharp
public AxisTimeUnit MajorUnitScale { get; set; }
```

## Notlar

Özellik yalnızca zaman kategorisi eksenleri için etkilidir.

## Örnekler

Bir grafik ekseninin işaretlerinin ve görüntülenen değerlerinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Y ekseninin küçük işaretlerini çizim alanından uzağa bakacak şekilde ayarlayın,
// ve ekseni geçmek için büyük işaretler.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Y eksenini her 10 birimde bir büyük bir işaret ve her 1 birimde bir küçük bir işaret gösterecek şekilde ayarlayın.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Y ekseninin sınırlarını -10 ve 20 olarak ayarlayın.
// Bu Y ekseni artık 4 ana işaret ve 27 küçük işaret gösterecek.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// X ekseni için, ana işaret noktalarını her 10 birimde bir ayarlayın,
// her küçük tik işareti 2,5 birimde.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Her iki tür işaretin de grafik çizim alanı içerisinde görünmesini yapılandırın.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// X ekseninin sınırlarını, X ekseninin 5 ana çizgi ve 12 küçük çizgiyi kapsayacak şekilde ayarlayın.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Tik etiketlerini milyon cinsinden değerlerini gösterecek şekilde ayarlayın.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Tik etiketlerinin değerlerini hangi değere göre görüntüleyeceğini daha spesifik bir değere ayarlayabiliriz.
// Bu ifade yukarıdaki ifadeye eşdeğerdir.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Ayrıca bakınız

* enum [AxisTimeUnit](../../axistimeunit/)
* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
