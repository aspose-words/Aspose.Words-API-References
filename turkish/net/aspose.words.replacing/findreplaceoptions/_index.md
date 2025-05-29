---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: .NET için Aspose.Words
description: Gelişmiş bul ve değiştir özellikleri için Aspose.Words.FindReplaceOptions sınıfını keşfedin; belge düzenlemeyi hassasiyet ve esneklikle geliştirin.
type: docs
weight: 5350
url: /tr/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Bul/değiştir işlemleri için seçenekleri belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bul ve Değiştir](https://docs.aspose.com/words/net/find-and-replace/) belgeleme makalesi.

```csharp
public class FindReplaceOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | FindReplaceOptions sınıfının yeni bir örneğini varsayılan ayarlarla başlatır. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | Belirtilen yönde FindReplaceOptions sınıfının yeni bir örneğini başlatır. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | Belirtilen değiştirme geri aramasıyla FindReplaceOptions sınıfının yeni bir örneğini başlatır. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | Belirtilen yön ve geri aramayı değiştirerek FindReplaceOptions sınıfının yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Yeni içeriğe uygulanan metin biçimlendirmesi. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Yeni içeriğe uygulanan paragraf biçimlendirmesi. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Değiştirme yönünü seçer. Varsayılan değerForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True, eskiDeğer'in bağımsız bir sözcük olması gerektiğini belirtir. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Silinen revizyonların içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Alan kodları içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Alanların içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Dipnotları yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Ekleme revizyonları içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Bir metin içindeki şekillerin göz ardı edileceğini belirten bir Boole değeri alır veya ayarlar. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | İçeriği yoksaymayı belirten bir Boole değeri alır veya ayarlar[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Varsayılan değer`YANLIŞ` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Eski bul/değiştir algoritmasının kullanıldığını belirten bir Boole değeri alır veya ayarlar. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True, büyük/küçük harfe duyarlı karşılaştırmayı, false ise büyük/küçük harfe duyarsız karşılaştırmayı gösterir. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | Değiştirmenin biçimini belirtir. Varsayılan değer:Text . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Her değiştirme oluşumundan önce çağrılan kullanıcı tanımlı yöntem. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Sonraki kardeş paragraf olmadığında paragraf break 'nin değiştirilmesine izin verilip verilmediğini belirten bir Boole değeri alır veya ayarlar. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True, metin kutuları dikkate alınarak yukarıdan aşağıya doğru bir metin aramasının gerçekleştirildiğini gösterir. Varsayılan değer`YANLIŞ` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Değiştirme kalıpları içinde değiştirmelerin tanınıp tanınmayacağını ve kullanılıp kullanılmayacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` . |

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

Bağımsız kelime bazlı bul ve değiştir işlemlerinin nasıl açılıp kapatılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bulunan metin başka bir kelimenin parçası değilse, onu değiştirmek için "FindWholeWordsOnly" bayrağını "true" olarak ayarlayın.
// Çevresindekilere bakılmaksızın tüm metni değiştirmek için "FindWholeWordsOnly" bayrağını "false" olarak ayarlayın.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Replacing](../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../)
