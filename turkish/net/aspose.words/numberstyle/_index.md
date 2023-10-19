---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words for .NET
description: Aspose.Words.NumberStyle Sıralama. Bir listenin dipnotların ve son notların sayfa numaralarının sayı stilini belirtir C#'da.
type: docs
weight: 4310
url: /tr/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Bir listenin, dipnotların ve son notların, sayfa numaralarının sayı stilini belirtir.

```csharp
public enum NumberStyle
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Arabic | `0` | Arapça numaralandırma (1, 2, 3, ...) |
| UppercaseRoman | `1` | Büyük harf Roma (I, II, III, ...) |
| LowercaseRoman | `2` | Küçük harf Roma (i, ii, iii, ...) |
| UppercaseLetter | `3` | Büyük Harf (A, B, C, ...) |
| LowercaseLetter | `4` | Küçük harf (a, b, c, ...) |
| Ordinal | `5` | Sıra (1., 2., 3., ...) |
| Number | `6` | Numaralı (Bir, İki, Üç, ...) |
| OrdinalText | `7` | Sıra (metin) (Birinci, İkinci, Üçüncü, ...) |
| Hex | `8` | Onaltılı: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicago Stil El Kitabı: *, †, † |
| Kanji | `10` | İdeograph-digital |
| KanjiDigit | `11` | Japonca sayma |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Tam genişlikte Arapça: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Yarı genişlikte Arapça: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japonca legal |
| KanjiTraditional2 | `17` | Japon dijital on bin |
| NumberInCircle | `18` | Kapalı daireler |
| DecimalFullWidth | `19` | Ondalık tam genişlik: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo tam genişlik |
| Iroha | `21` | Iroha tam genişlik |
| LeadingZero | `22` | Baştaki Sıfır (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Madde işareti (metindeki karakter kodunu kontrol edin) |
| Ganada | `24` | Kore Ganadası |
| Chosung | `25` | Kore Chosung |
| GB1 | `26` | Kapalı tam durak |
| GB2 | `27` | Kapalı parantez |
| GB3 | `28` | Kapalı daire Çince |
| GB4 | `29` | İdeograf kapalı daire |
| Zodiac1 | `30` | Geleneksel ideograf |
| Zodiac2 | `31` | İdeograf Burcu |
| Zodiac3 | `32` | Geleneksel İdeograf Burcu |
| TradChinNum1 | `33` | Tayvan sayımı |
| TradChinNum2 | `34` | İdeograf yasal geleneksel |
| TradChinNum3 | `35` | Tayvanlı sayma bin |
| TradChinNum4 | `36` | Tayvan dijital |
| SimpChinNum1 | `37` | Çince sayma |
| SimpChinNum2 | `38` | Basitleştirilmiş Çince yasal |
| SimpChinNum3 | `39` | Çince sayma bin |
| SimpChinNum4 | `40` | Çince (uygulanmadı) |
| HanjaRead | `41` | Kore dijitali |
| HanjaReadDigit | `42` | Korece sayma |
| Hangul | `43` | Kore legal |
| Hanja | `44` | Kore dijital2 |
| Hebrew1 | `45` | İbranice-1 |
| Arabic1 | `46` | Arapça alpha |
| Hebrew2 | `47` | İbranice-2 |
| Arabic2 | `48` | Arapça abjad |
| HindiLetter1 | `49` | Hintçe sesli harfler |
| HindiLetter2 | `50` | Hintçe ünsüzler |
| HindiArabic | `51` | Hintçe sayılar |
| HindiCardinalText | `52` | Hintçe tanımlayıcı (kardinaller) |
| ThaiLetter | `53` | Tay harfleri |
| ThaiArabic | `54` | Tayland rakamları |
| ThaiCardinalText | `55` | Tayca tanımlayıcı (kardinaller) |
| VietCardinalText | `56` | Vietnamca tanımlayıcı (kardinaller) |
| NumberInDash | `57` | Sayfa numarası formatı: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Küçük Rus alfabesi |
| UppercaseRussian | `59` | Büyük Rus alfabesi |
| None | `255` | Madde işareti veya numara yok. |
| Custom | `65280` | Özel sayı biçimi. Yalnızca DOCX formatı tarafından desteklenir. |

## Örnekler

DocumentBuilder kullanılırken özel liste formatının paragraflara nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve liste seviyelerinin ilk ikisini özelleştirin.
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

// Bu NumberFormat değeri yıldız şekilli madde işareti listesi sembolleri oluşturacaktır.
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
