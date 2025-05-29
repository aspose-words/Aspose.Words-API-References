---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: .NET için Aspose.Words
description: FindReplaceOptions'daki MatchCase özelliğini keşfedin, hassas metin düzenleme için büyük/küçük harfe duyarlı veya büyük/küçük harfe duyarsız karşılaştırmaları etkinleştirin. İş akışınızı optimize edin!
type: docs
weight: 140
url: /tr/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True, büyük/küçük harfe duyarlı karşılaştırmayı, false ise büyük/küçük harfe duyarsız karşılaştırmayı gösterir.

```csharp
public bool MatchCase { get; set; }
```

## Örnekler

Bul ve değiştir işlemi gerçekleştirirken büyük/küçük harf duyarlılığının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Değiştirilecek dizeleri bulurken büyük/küçük harf duyarlılığını uygulamak için "MatchCase" bayrağını "true" olarak ayarlayın.
// Değiştirilecek metni ararken karakter büyük/küçük harf ayrımını göz ardı etmek için "MatchCase" bayrağını "false" olarak ayarlayın.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
