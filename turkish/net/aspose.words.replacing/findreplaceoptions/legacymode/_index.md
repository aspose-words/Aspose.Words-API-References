---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: Aspose.Words for .NET
description: FindReplaceOptions LegacyMode mülk. Eski bul/değiştir algoritmasının kullanıldığını belirten bir boole değeri alır veya ayarlar C#'da.
type: docs
weight: 130
url: /tr/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Eski bul/değiştir algoritmasının kullanıldığını belirten bir boole değeri alır veya ayarlar.

```csharp
public bool LegacyMode { get; set; }
```

## Notlar

Gelişmiş bul/değiştir özelliğinin tanıtılmasından önceki davranışın tam olarak aynısına ihtiyacınız varsa bu bayrağı kullanın. Eski algoritmanın, aralarla değiştirme, biçimlendirme uygulama vb. gibi gelişmiş özellikleri desteklemediğini unutmayın.

## Örnekler

Değiştirme kalıpları içindeki değiştirmelerin nasıl tanınacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Eski modun kullanılması birçok gelişmiş özelliği desteklemez, dolayısıyla onu 'yanlış' olarak ayarlamamız gerekir.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
