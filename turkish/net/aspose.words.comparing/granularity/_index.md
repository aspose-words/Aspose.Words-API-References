---
title: Enum Granularity
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Comparing.Granularity Sıralama. İki belgeyi karşılaştırırken izlenecek değişikliklerin ayrıntı düzeyini belirtir.
type: docs
weight: 280
url: /tr/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

İki belgeyi karşılaştırırken izlenecek değişikliklerin ayrıntı düzeyini belirtir.

```csharp
public enum Granularity
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

### Örnekler

Belgeleri karşılaştırırken bir ayrıntı düzeyi belirtmek için gösterir.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Değişikliklerin izlenip izlenmediğini belirtin
// karaktere göre ('Granularity.CharLevel') veya kelimeye göre ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// İlk belgenin revizyon grupları koleksiyonu, belgeler arasındaki tüm farklılıkları içerir.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Comparing](../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../)


