---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: .NET için Aspose.Words
description: Belge değişikliklerini hassasiyetle zahmetsizce izlemek için Aspose.Words.Comparing.Granularity enum'unu keşfedin. Belge karşılaştırmanızı bugün geliştirin!
type: docs
weight: 490
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
| CharLevel | `0` | Karakter düzeyindeki değişiklikleri belirtir. |
| WordLevel | `1` | Kelime düzeyindeki değişiklikleri belirtir. |

## Örnekler

Belgeleri karşılaştırırken ayrıntı düzeyini belirtmek için kullanılır.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Değişikliklerin izlenip izlenmediğini belirtin
// karaktere göre ('Granularity.CharLevel') veya kelimeye göre ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// İlk belgenin revizyon grupları koleksiyonu, belgeler arasındaki tüm farklılıkları içerir.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Comparing](../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../)
