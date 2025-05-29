---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: .NET için Aspose.Words
description: ConvertUtil'in PixelToNewDpi yöntemi ile piksel çözünürlüklerini zahmetsizce dönüştürün. Projeleriniz için optimum görüntü kalitesi ve hassasiyeti elde edin.
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
| oldDpi | Double | Mevcut dpi (inç başına nokta sayısı) çözünürlüğü. |
| newDpi | Double | Yeni dpi (inç başına nokta sayısı) çözünürlüğü. |

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
