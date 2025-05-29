---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: .NET için Aspose.Words
description: FindReplaceOptions'daki UseSubstitutions özelliğini keşfedin. Gelişmiş metin düzenleme esnekliği için değiştirme desenlerinde değiştirmeleri kolayca etkinleştirin.
type: docs
weight: 190
url: /tr/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Değiştirme kalıpları içinde değiştirmelerin tanınıp tanınmayacağını ve kullanılıp kullanılmayacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Notlar

İkame öğeleriyle ilgili ayrıntılar için lütfen şuraya bakın: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

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

Metnin ikamelerle nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// "UseSubstitutions" özelliğini "true" olarak ayarlayın
// ikame öğelerini tanımak için bul-ve-değiştir işlemi.
// İkame öğelerini yok saymak için "UseSubstitutions" özelliğini "false" olarak ayarlayın.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
