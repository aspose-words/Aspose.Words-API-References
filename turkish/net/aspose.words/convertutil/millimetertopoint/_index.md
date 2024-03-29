---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words for .NET
description: ConvertUtil MillimeterToPoint yöntem. Milimetreyi noktaya dönüştürür C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Milimetreyi noktaya dönüştürür.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| millimeters | Double | Dönüştürülecek değer. |

## Notlar

1 inç, 25,4 milimetreye eşittir. 1 inç 72 puana eşittir.

## Örnekler

Sayfa özelliklerinin milimetre cinsinden nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir bölümün "Sayfa Yapısı" sayfa kenar boşluklarının boyutunu nokta cinsinden tanımlar.
// Daha tanıdık bir ölçü birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz,
// sınırları tanımlarken milimetre gibi.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// Bir santimetre yaklaşık 28,3 puandır.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Yeni kenar boşluklarını gösterecek içerik ekleyin.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Ayrıca bakınız

* class [ConvertUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
