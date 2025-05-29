---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: .NET için Aspose.Words
description: Metin parçalarından Küme nesnelerini verimli bir şekilde üreten, hassas metin biçimlendirmesi ve hizalaması sağlayan iTextShaper'ın ShapeText yöntemini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Geri Döndürür[`Cluster`](../../cluster/)metin parçalarından oluşan bir diziden üretilen nesneler. Döndürülen dizinin uzunluğu, uzunluğuna eşittir*runs* . Bir dizinde çalıştırılan kümelere karşılık gelen kümeler varsa, aynı dizindeki sonuç bunları kaydeder.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| runs | String[] | Bir dizi metin parçası |
| direction | Direction | Bir metin yönü |
| script | UnicodeScript | Bir senaryo |
| enabledFontFeatures | FontFeature[] | Dikkate alınması gereken açıkça etkinleştirilmiş bir dizi OpenType özelliği |
| variations | VariationAxisCoordinate[] | Font'un varyasyon ekseni değerleri |

### Ayrıca bakınız

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* ad alanı [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* toplantı [Aspose.Words](../../../)
