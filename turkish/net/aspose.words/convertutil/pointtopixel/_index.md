---
title: ConvertUtil.PointToPixel
second_title: Aspose.Words for .NET API Referansı
description: ConvertUtil yöntem. Noktaları 96 dpide piksellere dönüştürür.
type: docs
weight: 60
url: /tr/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(double) {#pointtopixel}

Noktaları 96 dpi'de piksellere dönüştürür.

```csharp
public static double PointToPixel(double points)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Dönüştürülecek değer. |

### Notlar

1 inç, 72 noktaya eşittir.

### Örnekler

Sayfa özelliklerinin piksel cinsinden nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir bölümün "Sayfa Yapısı", sayfa kenar boşluklarının boyutunu nokta olarak tanımlar.
// Farklı bir ölçü birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz,
// sınırları tanımlarken pikseller gibi.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// Bir piksel 0,75 puandır.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// Kullanılan varsayılan DPI değeri 96'dır.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Yeni kenar boşluklarını göstermek için içerik ekleyin.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Ayrıca bakınız

* class [ConvertUtil](../)
* ad alanı [Aspose.Words](../../convertutil/)
* toplantı [Aspose.Words](../../../)

---

## PointToPixel(double, double) {#pointtopixel_1}

Belirtilen piksel çözünürlüğünde noktaları piksellere dönüştürür.

```csharp
public static double PointToPixel(double points, double resolution)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Dönüştürülecek değer. |
| resolution | Double | dpi (inç başına nokta) çözünürlüğü. |

### Notlar

1 inç, 72 noktaya eşittir.

### Örnekler

Varsayılan ve özel çözünürlükle piksellere dönüştürme noktalarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu bölümün üst kenar boşluğunun boyutunu, özel bir DPI'ye göre piksel cinsinden tanımlayın.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// 96'lık varsayılan DPI'da bir piksel 0,75 puandır.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Yeni bir DPI ayarlayın ve üst kenar boşluğu değerini buna göre ayarlayın.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Ayrıca bakınız

* class [ConvertUtil](../)
* ad alanı [Aspose.Words](../../convertutil/)
* toplantı [Aspose.Words](../../../)


