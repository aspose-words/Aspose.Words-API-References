---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: .NET için Aspose.Words
description: CompareOptions Granularity özelliğini keşfedin, hassas metin düzenleme için karakter veya kelime bazında değişiklikleri izleyin. Belge kontrolünüzü bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Değişikliklerin karakter bazında mı yoksa kelime bazında mı izlendiğini belirtir.

```csharp
public Granularity Granularity { get; set; }
```

## Notlar

Varsayılan değerWordLevel .

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* ad alanı [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* toplantı [Aspose.Words](../../../)
