---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: .NET için Aspose.Words
description: Gelişmiş işlevsellik ve kusursuz kullanıcı deneyimi için klasik bul/değiştir algoritmasını kolayca açıp kapatmak üzere FindReplaceOptions LegacyMode özelliğini keşfedin.
type: docs
weight: 130
url: /tr/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Eski bul/değiştir algoritmasının kullanıldığını belirten bir Boole değeri alır veya ayarlar.

```csharp
public bool LegacyMode { get; set; }
```

## Notlar

Gelişmiş bul/değiştir özelliği tanıtılmadan önce olduğu gibi aynı davranışa ihtiyacınız varsa bu bayrağı kullanın. Eski algoritmanın kesmelerle değiştirme, biçimlendirme uygulama vb. gibi gelişmiş özellikleri desteklemediğini unutmayın.

## Örnekler

Yer değiştirme kalıpları içindeki yer değiştirmelerin nasıl tanınacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Eski modu kullanmak pek çok gelişmiş özelliği desteklemez, bu yüzden bunu 'false' olarak ayarlamamız gerekir.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
