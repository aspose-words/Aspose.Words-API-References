---
title: Class FindReplaceOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Replacing.FindReplaceOptions sınıf. Bul/değiştir işlemlerine ilişkin seçenekleri belirtir.
type: docs
weight: 4620
url: /tr/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Bul/değiştir işlemlerine ilişkin seçenekleri belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bul ve Değiştir](https://docs.aspose.com/words/net/find-and-replace/) dokümantasyon makalesi.

```csharp
public class FindReplaceOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Yeni içeriğe uygulanan metin formatı. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Yeni içeriğe paragraf biçimlendirmesi uygulandı. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Değiştirme yönünü seçer. Varsayılan değer:Forward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True, eskiDeğer'in bağımsız bir sözcük olması gerektiğini belirtir. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Silme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Alan kodları içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Alanların içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Dipnotların yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Ekleme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Bir metin içindeki şekillerin yoksayılacağını belirten bir boole değeri alır veya ayarlar. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | İçeriğin yoksayılacağını belirten bir boole değeri alır veya ayarlar.[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Varsayılan değer:`YANLIŞ` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Eski bul/değiştir algoritmasının kullanıldığını belirten bir boole değeri alır veya ayarlar. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True büyük/küçük harfe duyarlı karşılaştırmayı, false ise büyük/küçük harfe duyarlı olmayan karşılaştırmayı belirtir. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Her değiştirme işleminden önce çağrılan kullanıcı tanımlı yöntem. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Sonraki eş paragraf olmadığında break paragrafının değiştirilmesine izin verildiğini belirten bir boole değeri alır veya ayarlar. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True, metin kutuları dikkate alınarak yukarıdan aşağıya doğru sırayla metin araması yapıldığını belirtir. Varsayılan değer:`YANLIŞ` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Değiştirme kalıpları içindeki ikamelerin tanınıp kullanılmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` . |

### Örnekler

Bul ve değiştir işlemi gerçekleştirirken büyük/küçük harf duyarlılığının nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Değiştirilecek dizeleri bulurken büyük/küçük harf duyarlılığını uygulamak için "MatchCase" bayrağını "true" olarak ayarlayın.
// Değiştirilecek metni ararken karakter büyük/küçük harf durumunu dikkate almamak için "MatchCase" bayrağını "false" olarak ayarlayın.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Bağımsız salt sözcük bul ve değiştir işlemlerinin nasıl değiştirileceğini gösterir.

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

* ad alanı [Aspose.Words.Replacing](../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../)


