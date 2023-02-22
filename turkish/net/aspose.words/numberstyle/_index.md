---
title: Enum NumberStyle
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.NumberStyle Sıralama. Bir liste dipnotlar ve son notlar sayfa numaraları için sayı stilini belirtir.
type: docs
weight: 4070
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
| UppercaseRoman | `1` | Büyük harf Roman (I, II, III, ...) |
| LowercaseRoman | `2` | Küçük Roman (i, ii, iii, ...) |
| UppercaseLetter | `3` | Büyük Harf (A, B, C, ...) |
| LowercaseLetter | `4` | Küçük harf (a, b, c, ...) |
| Ordinal | `5` | Sıra (1., 2., 3., ...) |
| Number | `6` | Numaralandırılmış (Bir, İki, Üç, ...) |
| OrdinalText | `7` | Sıra (metin) (Birinci, İkinci, Üçüncü, ...) |
| Hex | `8` | Onaltılı: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Chicago Stil El Kitabı: *, †, † |
| Kanji | `10` | Ideograph-digital |
| KanjiDigit | `11` | Japonca sayma |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Iroha |
| ArabicFullWidth | `14` | Tam genişlikte Arapça: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Yarım genişlikte Arapça: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Japonca yasal |
| KanjiTraditional2 | `17` | Japonca dijital on bin |
| NumberInCircle | `18` | Kapalı çevreler |
| DecimalFullWidth | `19` | Ondalık tam genişlik: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo tam genişlik |
| Iroha | `21` | Iroha tam genişlik |
| LeadingZero | `22` | Başta Sıfır (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Madde işareti (metindeki karakter kodunu kontrol edin) |
| Ganada | `24` | Korece Ganada |
| Chosung | `25` | Kore Chosung |
| GB1 | `26` | Kapalı tam durak |
| GB2 | `27` | Kapalı parantez |
| GB3 | `28` | Kapalı daire Chinese |
| GB4 | `29` | İdeograf kapalı daire |
| Zodiac1 | `30` | İdeograf geleneksel |
| Zodiac2 | `31` | İdeograf Zodiac |
| Zodiac3 | `32` | İdeograf Burç geleneksel |
| TradChinNum1 | `33` | Tayvanlı sayma |
| TradChinNum2 | `34` | Ideograph yasal geleneksel |
| TradChinNum3 | `35` | bin Tayvanlı sayılıyor |
| TradChinNum4 | `36` | Tayvanlı digital |
| SimpChinNum1 | `37` | Çince sayma |
| SimpChinNum2 | `38` | Çince yasal basitleştirilmiş |
| SimpChinNum3 | `39` | Çince sayma bin |
| SimpChinNum4 | `40` | Çince (uygulanmadı) |
| HanjaRead | `41` | Korece dijital |
| HanjaReadDigit | `42` | Korece sayma |
| Hangul | `43` | Kore yasal |
| Hanja | `44` | Kore digital2 |
| Hebrew1 | `45` | İbranice-1 |
| Arabic1 | `46` | Arapça alpha |
| Hebrew2 | `47` | İbranice-2 |
| Arabic2 | `48` | Arapça abjad |
| HindiLetter1 | `49` | Hintçe ünlüler |
| HindiLetter2 | `50` | Hintçe ünsüzleri |
| HindiArabic | `51` | Hintçe sayılar |
| HindiCardinalText | `52` | Hintçe açıklayıcı (kardinaller) |
| ThaiLetter | `53` | Tay harfleri |
| ThaiArabic | `54` | Tay numaraları |
| ThaiCardinalText | `55` | Tayca açıklayıcı (kardinaller) |
| VietCardinalText | `56` | Vietnamca açıklayıcı (kardinaller) |
| NumberInDash | `57` | Sayfa numarası biçimi: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Küçük Rus alfabesi |
| UppercaseRussian | `59` | Büyük Rus alfabesi |
| None | `255` | Madde işareti veya sayı yok. |
| Custom | `65280` | Özel sayı biçimi. Yalnızca DOCX biçimi tarafından desteklenir. |

### Örnekler

DocumentBuilder kullanılırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Bir Microsoft Word şablonundan bir liste oluşturun ve liste düzeylerinin ilk ikisini özelleştirin.
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

// Bu NumberFormat değeri, yıldız şeklinde madde işareti listesi sembolleri oluşturacaktır.
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


