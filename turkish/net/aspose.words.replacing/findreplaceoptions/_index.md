---
title: FindReplaceOptions
second_title: Aspose.Words for .NET API Referansı
description: Bul/değiştir işlemleri için seçenekleri belirtir.
type: docs
weight: 4360
url: /tr/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Bul/değiştir işlemleri için seçenekleri belirtir.

```csharp
public class FindReplaceOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont) { get; } | Yeni içeriğe metin biçimlendirme uygulandı. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat) { get; } | Paragraf biçimlendirmesi yeni içeriğe uygulandı. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction) { get; set; } | Değiştirilecek yönü seçer. Varsayılan değerForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly) { get; set; } | True, eskiDeğerin bağımsız bir sözcük olması gerektiğini belirtir. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted) { get; set; } | Silme revizyonları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes) { get; set; } | Alan kodları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields) { get; set; } | Alanların içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes) { get; set; } | Dipnotların yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted) { get; set; } | Ekleme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer`yanlış` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode) { get; set; } | Eski bul/değiştir algoritmasının kullanıldığını gösteren bir boole değeri alır veya ayarlar. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase) { get; set; } | True, büyük/küçük harf duyarlı karşılaştırmayı, false ise büyük/küçük harf duyarlı karşılaştırmayı belirtir. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback) { get; set; } | Her değiştirme oluşumundan önce çağrılan kullanıcı tanımlı yöntem. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement) { get; set; } | Sonraki kardeş paragraf olmadığında break paragrafının değiştirilmesine izin verildiğini belirten bir boole değeri alır veya ayarlar. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder) { get; set; } | True, bir metin aramasının metin kutuları dikkate alınarak yukarıdan aşağıya sırayla gerçekleştirildiğini belirtir. Varsayılan değer false'dir. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions) { get; set; } | Değiştirme kalıpları içindeki ikamelerin tanınıp tanınmayacağını ve kullanılıp kullanılmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer şudur:`yanlış` . |

### Örnekler

Bul ve değiştir işlemi gerçekleştirirken büyük/küçük harf duyarlılığının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Değiştirilecek dizeleri bulurken büyük/küçük harf duyarlılığı uygulamak için "MatchCase" bayrağını "true" olarak ayarlayın.
// Değiştirilecek metni ararken büyük/küçük harf harflerini yok saymak için "MatchCase" bayrağını "false" olarak ayarlayın.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Yalnızca sözcükten oluşan bağımsız bul ve değiştir işlemlerinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bulunan metni başka bir kelimenin parçası değilse değiştirmek için "FindWholeWordsOnly" bayrağını "true" olarak ayarlayın.
// Çevresinden bağımsız olarak tüm metni değiştirmek için "FindWholeWordsOnly" bayrağını "false" olarak ayarlayın.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Replacing](../../aspose.words.replacing)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
