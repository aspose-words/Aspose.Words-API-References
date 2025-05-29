---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: .NET için Aspose.Words
description: ConvertUtil'in PointToInch yöntemi ile noktaları zahmetsizce inçlere dönüştürün. Ölçümlerinizi basitleştirin ve tasarım doğruluğunuzu bugün artırın!
type: docs
weight: 50
url: /tr/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Noktaları inçlere dönüştürür.

```csharp
public static double PointToInch(double points)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| points | Double | Dönüştürülecek değer. |

## Notlar

1 inç 72 puana eşittir.

## Örnekler

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

* class [ConvertUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
