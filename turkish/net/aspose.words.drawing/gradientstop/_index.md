---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: .NET için Aspose.Words
description: Geliştirilmiş belge görselleri için özelleştirilebilir duraklarla çarpıcı degradeler oluşturma çözümünüz olan Aspose.Words.Drawing.GradientStop sınıfını keşfedin.
type: docs
weight: 1310
url: /tr/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Bir gradyan durağını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafik Öğelerle Çalışma](https://docs.aspose.com/words/net/working-with-graphic-elements/) belgeleme makalesi.

```csharp
public class GradientStop
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Yeni bir örneğini başlatır`GradientStop` sınıf. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Yeni bir örneğini başlatır`GradientStop` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Herhangi bir değiştirici kullanmadan degrade durağının rengini temsil eden bir değer alır. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Degrade durağının rengini temsil eden bir değer alır veya ayarlar. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Gradyan içindeki bir durağın konumunu temsil eden bir değeri alır veya ayarlar. 0,0 ile 1,0 aralığında bir yüzde olarak ifade edilir. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Degradenin şeffaflığını temsil eden bir değeri alır veya ayarlar fill 0,0 ile 1,0 aralığında bir yüzde olarak ifade edilir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Üst öğeden degrade durağını kaldırır[`GradientStopCollection`](../gradientstopcollection/) . |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
