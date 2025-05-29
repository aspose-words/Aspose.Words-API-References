---
title: ConvertUtil Class
linktitle: ConvertUtil
articleTitle: ConvertUtil
second_title: .NET için Aspose.Words
description: Kusursuz birim dönüşümü için Aspose.Words.ConvertUtil sınıfını keşfedin. Belge işlemenizi bugün temel yardımcı işlevlerle geliştirin!
type: docs
weight: 560
url: /tr/net/aspose.words/convertutil/
---
## ConvertUtil class

Çeşitli ölçüm birimleri arasında dönüşüm yapmak için yardımcı işlevler sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Ölçüm Birimleri Arasında Dönüşüm](https://docs.aspose.com/words/net/convert-between-measurement-units/) belgeleme makalesi.

```csharp
public static class ConvertUtil
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(*double*) | İnçleri noktalara dönüştürür. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(*double*) | Milimetreleri noktalara dönüştürür. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(*double, double, double*) | Pikselleri bir çözünürlükten diğerine dönüştürür. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(*double*) | Pikselleri 96 dpi'da noktalara dönüştürür. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(*double, double*) | Pikselleri belirtilen piksel çözünürlüğündeki noktalara dönüştürür. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(*double*) | Noktaları inçlere dönüştürür. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(*double*) | Noktaları 96 dpi'da piksellere dönüştürür. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(*double, double*) | Noktaları belirtilen piksel çözünürlüğünde piksellere dönüştürür. |

## Örnekler

Bir bölüm için kağıt boyutunun, yönlendirmenin, kenar boşluklarının ve diğer ayarların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Sayfa özelliklerinin inç cinsinden nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir bölümün "Sayfa Düzeni" sayfa kenar boşluklarının boyutunu nokta cinsinden tanımlar.
// Daha tanıdık bir ölçüm birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz.
// Sınırları tanımlarken inç gibi.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Bir inç 72 puandır.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Yeni kenar boşluklarını gösteren içerik ekleyin.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
