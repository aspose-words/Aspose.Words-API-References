---
title: Class GradientStopCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.GradientStopCollection sınıf. Şunların bir koleksiyonunu içerirGradientStop nesneler.
type: docs
weight: 990
url: /tr/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

Şunların bir koleksiyonunu içerir:[`GradientStop`](../gradientstop/) nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafik Öğeleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-graphic-elements/) dokümantasyon makalesi.

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | Koleksiyondaki öğelerin sayısını belirten bir tamsayı değeri alır. |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | Bir değeri alır veya ayarlar[`GradientStop`](../gradientstop/) koleksiyondaki nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(GradientStop) | Belirtilen değeri ekler[`GradientStop`](../gradientstop/) bir degradeye. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | Koleksiyonda yinelenen bir numaralandırıcı döndürür. |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(int, GradientStop) | Bir ekler[`GradientStop`](../gradientstop/) belirtilen indeksteki koleksiyona. |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(GradientStop) | Belirtilen bir öğeyi kaldırır[`GradientStop`](../gradientstop/) koleksiyondan. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(int) | Bir'i kaldırır[`GradientStop`](../gradientstop/) belirtilen dizindeki koleksiyondan. |

### Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. [`GradientStops`](../fill/gradientstops/)dolgu nesnelerinin degrade duraklarına erişme özelliği.

### Örnekler

Degrade dolgusuna degrade duraklarının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Degrade durakları koleksiyonunu alın.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// İlk degrade durağını değiştirin.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Koleksiyonun sonuna yeni degrade durağı ekleyin.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Dizin 1'deki degrade durağını kaldırın.
gradientStops.RemoveAt(1);
// Ve aynı indeks 1'e yeni degrade durağı ekleyin.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Koleksiyondaki son degrade durağını kaldırın.
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

* class [GradientStop](../gradientstop/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


