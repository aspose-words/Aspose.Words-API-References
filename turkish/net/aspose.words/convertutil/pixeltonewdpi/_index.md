---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words for .NET
description: ConvertUtil PixelToNewDpi yöntem. Pikselleri bir çözünürlükten diğerine dönüştürür C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Pikselleri bir çözünürlükten diğerine dönüştürür.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| pixels | Double | Dönüştürülecek değer. |
| oldDpi | Double | Geçerli dpi (inç başına nokta sayısı) çözünürlüğü. |
| newDpi | Double | Yeni dpi (inç başına nokta sayısı) çözünürlüğü. |

## Örnekler

Varsayılan ve özel çözünürlükle piksellere dönüştürme noktalarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Özel DPI'ya göre bu bölümün üst kenar boşluğunun boyutunu piksel cinsinden tanımlayın.
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
