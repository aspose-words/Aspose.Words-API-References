---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words for .NET
description: CompareOptions Granularity mülk. Değişikliklerin karaktere göre mi yoksa kelimeye göre mi izleneceğini belirtir. Varsayılan değerWordLevel  C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Değişikliklerin karaktere göre mi yoksa kelimeye göre mi izleneceğini belirtir. Varsayılan değer:WordLevel .

```csharp
public Granularity Granularity { get; set; }
```

## Örnekler

Belgeleri karşılaştırırken ayrıntı düzeyini belirtmeyi gösterir.

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
