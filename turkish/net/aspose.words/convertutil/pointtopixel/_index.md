---
title: ConvertUtil.PointToPixel
linktitle: PointToPixel
articleTitle: PointToPixel
second_title: .NET için Aspose.Words
description: ConvertUtil'in 96 dpi için optimize edilmiş PointToPixel yöntemi ile noktaları zahmetsizce piksellere dönüştürün. Tasarım hassasiyetinizi bugün artırın!
type: docs
weight: 60
url: /tr/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(*double*) {#pointtopixel}

Noktaları 96 dpi'da piksellere dönüştürür.

```csharp
public static double PointToPixel(double points)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Dönüştürülecek değer. |

## Notlar

1 inç 72 puana eşittir.

## Örnekler

Sayfa özelliklerinin piksel cinsinden nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir bölümün "Sayfa Düzeni" sayfa kenar boşluklarının boyutunu nokta cinsinden tanımlar.
// Farklı bir ölçüm birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz.
// Sınırları tanımlarken piksel gibi.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// Bir piksel 0,75 noktadır.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// Varsayılan olarak kullanılan DPI değeri 96'dır.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Yeni kenar boşluklarını gösteren içerik ekleyin.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Ayrıca bakınız

* class [ConvertUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## PointToPixel(*double, double*) {#pointtopixel_1}

Noktaları belirtilen piksel çözünürlüğünde piksellere dönüştürür.

```csharp
public static double PointToPixel(double points, double resolution)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Dönüştürülecek değer. |
| resolution | Double | Dpi (inç başına nokta sayısı) çözünürlüğü. |

## Notlar

1 inç 72 puana eşittir.

## Örnekler

Varsayılan ve özel çözünürlükle noktaların piksellere nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu bölümün üst kenar boşluğunun boyutunu özel bir DPI'a göre piksel cinsinden tanımlayın.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Varsayılan 96 DPI'da bir piksel 0,75 puandır.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Yeni bir DPI belirleyin ve üst kenar boşluğu değerini buna göre ayarlayın.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Ayrıca bakınız

* class [ConvertUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
