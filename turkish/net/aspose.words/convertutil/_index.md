---
title: Class ConvertUtil
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.ConvertUtil sınıf. Çeşitli ölçüm birimleri arasında dönüştürme yapmak için yardımcı işlevler sağlar.
type: docs
weight: 360
url: /tr/net/aspose.words/convertutil/
---
## ConvertUtil class

Çeşitli ölçüm birimleri arasında dönüştürme yapmak için yardımcı işlevler sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Ölçü Birimleri Arasında Dönüştürme](https://docs.aspose.com/words/net/convert-between-measurement-units/) dokümantasyon makalesi.

```csharp
public static class ConvertUtil
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(double) | İnçleri noktalara dönüştürür. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(double) | Milimetreyi noktaya dönüştürür. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(double, double, double) | Pikselleri bir çözünürlükten diğerine dönüştürür. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(double) | Pikselleri 96 dpi'de noktalara dönüştürür. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(double, double) | Belirtilen piksel çözünürlüğünde pikselleri noktalara dönüştürür. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(double) | Noktaları inç'e dönüştürür. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(double) | Noktaları 96 dpi'de piksellere dönüştürür. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(double, double) | Noktaları belirtilen piksel çözünürlüğünde piksellere dönüştürür. |

### Örnekler

Bir bölüm için kağıt boyutunun, yönünün, kenar boşluklarının ve diğer ayarların nasıl ayarlanacağını gösterir.

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

// Bir bölümün "Sayfa Yapısı" sayfa kenar boşluklarının boyutunu nokta cinsinden tanımlar.
// Daha tanıdık bir ölçü birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz,
// sınırları tanımlarken inç gibi.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Bir inç 72 puandır.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Yeni kenar boşluklarını gösterecek içerik ekleyin.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


