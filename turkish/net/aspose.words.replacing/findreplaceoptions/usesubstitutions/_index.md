---
title: FindReplaceOptions.UseSubstitutions
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. Değiştirme kalıpları içindeki ikamelerin tanınıp kullanılmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 180
url: /tr/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Değiştirme kalıpları içindeki ikamelerin tanınıp kullanılmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool UseSubstitutions { get; set; }
```

### Notlar

İkame öğeleriyle ilgili ayrıntılar için lütfen şu adrese bakın: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

### Örnekler

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

Metnin değişikliklerle nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bunu elde etmek için "UseSubstitutions" özelliğini "true" olarak ayarlayın
// ikame elemanlarını tanımak için bul ve değiştir işlemi.
// Değiştirme öğelerini yok saymak için "UseSubstitutions" özelliğini "false" olarak ayarlayın.
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
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


