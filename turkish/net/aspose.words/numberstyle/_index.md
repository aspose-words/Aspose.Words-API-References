---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: .NET için Aspose.Words
description: Dipnot ve son not sayfa numaralarını özelleştirmek ve belge biçimlendirmenizi zahmetsizce geliştirmek için Aspose.Words.NumberStyle numaralandırmasını keşfedin.
type: docs
weight: 5040
url: /tr/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Bir liste, dipnotlar ve son notlar, sayfa numaraları için sayı stilini belirtir.

```csharp
public enum NumberStyle
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Arabic | `0` | Arapça numaralandırma (1, 2, 3, ...) |
| UppercaseRoman | `1` | Büyük harfli Roma (I, II, III, ...) |
| LowercaseRoman | `2` | Küçük harfli Roma (i, ii, iii, ...) |
| UppercaseLetter | `3` | Büyük Harf (A, B, C, ...) |
| LowercaseLetter | `4` | Küçük harf (a, b, c, ...) |
| Ordinal | `5` | Sıra (1., 2., 3., ...) |
| Number | `6` | Numaralandırılmış (Bir, İki, Üç, ...) |
| OrdinalText | `7` | Sıralı (metin) (Birinci, İkinci, Üçüncü, ...) |
| Hex | `8` | Onaltılık: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicago Stil Kılavuzu: *, †, † |
| Kanji | `10` | İdeogram-dijital |
| KanjiDigit | `11` | Japonca sayma |
| AiueoHalfWidth | `12` | Yardım |
| IrohaHalfWidth | `13` | İroha |
| ArabicFullWidth | `14` | Tam genişlikte Arapça: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Yarım genişlikte Arapça: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japonca yasal |
| KanjiTraditional2 | `17` | Japon dijital on bin |
| NumberInCircle | `18` | Kapalı daireler |
| DecimalFullWidth | `19` | Ondalık tam genişlik: 1, 2, 3, 4 |
| Aiueo | `20` | Yardımcı tam genişlik |
| Iroha | `21` | Iroha tam genişlik |
| LeadingZero | `22` | Önde Gelen Sıfır (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Madde işareti (metindeki karakter kodunu kontrol edin) |
| Ganada | `24` | Kore Ganadası |
| Chosung | `25` | Kore Chosung |
| GB1 | `26` | Kapalı nokta |
| GB2 | `27` | Kapalı parantez |
| GB3 | `28` | Çevrelenmiş daire Çince |
| GB4 | `29` | Daire içine alınmış ideogram |
| Zodiac1 | `30` | İdeogram geleneksel |
| Zodiac2 | `31` | İdeogram Zodyak |
| Zodiac3 | `32` | İdeogram Zodyak geleneksel |
| TradChinNum1 | `33` | Tayvan sayımı |
| TradChinNum2 | `34` | İdeogram yasal geleneksel |
| TradChinNum3 | `35` | Tayvanlılar binleri sayıyor |
| TradChinNum4 | `36` | Tayvan dijital |
| SimpChinNum1 | `37` | Çince sayma |
| SimpChinNum2 | `38` | Çince hukuki basitleştirilmiş |
| SimpChinNum3 | `39` | Çince bin sayma |
| SimpChinNum4 | `40` | Çince (uygulanmadı) |
| HanjaRead | `41` | Kore dijital |
| HanjaReadDigit | `42` | Korece sayma |
| Hangul | `43` | Kore yasal |
| Hanja | `44` | Kore dijital2 |
| Hebrew1 | `45` | İbranice-1 |
| Arabic1 | `46` | Arapça alfa |
| Hebrew2 | `47` | İbranice-2 |
| Arabic2 | `48` | Arapça ebced |
| HindiLetter1 | `49` | Hintçe ünlüler |
| HindiLetter2 | `50` | Hintçe ünsüzler |
| HindiArabic | `51` | Hintçe sayılar |
| HindiCardinalText | `52` | Hintçe betimleyici (kardinaller) |
| ThaiLetter | `53` | Tay harfleri |
| ThaiArabic | `54` | Tayca sayılar |
| ThaiCardinalText | `55` | Tayca betimleyici (kardinaller) |
| VietCardinalText | `56` | Vietnamca betimleyici (kardinaller) |
| NumberInDash | `57` | Sayfa numarası biçimi: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Küçük harfli Rus alfabesi |
| UppercaseRussian | `59` | Büyük harfli Rus alfabesi |
| None | `255` | Madde işareti veya numara yok. |
| Custom | `65280` | Özel sayı biçimi. Yalnızca DOCX biçimi tarafından desteklenir. |

## Örnekler

DocumentBuilder kullanılırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve liste düzeylerinin ilk ikisini özelleştirin.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Bu NumberFormat değeri yıldız şeklinde madde işaretli liste sembolleri oluşturacaktır.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Paragraflar oluşturun ve özel liste biçimlendirmemizin her iki liste düzeyini de bunlara uygulayın.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
