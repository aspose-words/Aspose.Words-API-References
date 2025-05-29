---
title: GradientStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: GradientStopCollection Ekleme yöntemiyle gradyanlarınızı zahmetsizce geliştirin. Canlı tasarımlar için özel GradientStop'ları sorunsuzca ekleyin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/gradientstopcollection/add/
---
## GradientStopCollection.Add method

Belirtilen bir öğeyi ekler[`GradientStop`](../../gradientstop/) bir eğime.

```csharp
public GradientStop Add(GradientStop gradientStop)
```

## Örnekler

Degrade dolgusuna degrade duraklarının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Degrade duraklarının toplanmasını sağla.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// İlk degrade durağını değiştir.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Koleksiyonun sonuna yeni bir degrade durağı ekle.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// 1. indeksteki degrade durağını kaldır.
gradientStops.RemoveAt(1);
// Ve aynı indeks 1'e yeni bir degrade durağı ekle.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Koleksiyondaki son degrade durağını kaldır.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Şekli DML kullanarak tanımlamak için uyumluluk seçeneğini kullanın
// belge kaydedildikten sonra "GradientStops" özelliğini almak istiyorsanız.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Ayrıca bakınız

* class [GradientStop](../../gradientstop/)
* class [GradientStopCollection](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
